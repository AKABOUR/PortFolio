<script setup>
import { ref } from 'vue';
import emailjs from 'emailjs-com';
import { useForm, useField } from 'vee-validate';
import * as yup from 'yup';

const dialog = ref(false);

// Validation
const schema = yup.object({
  nom: yup.string().required(),
  email: yup.string().email().required(),
  message: yup.string().required(),
});
const { handleSubmit, errors, resetForm  } = useForm({ validationSchema: schema });
const { value: nom } = useField('nom');
const { value: email } = useField('email');
const { value: message } = useField('message');

const sendForm = handleSubmit(async () => {
  try {
    const serviceId = import.meta.env.VITE_EMAILJS_SERVICE_ID;
    const templateId = import.meta.env.VITE_EMAILJS_TEMPLATE_ID;
    const publicKey = import.meta.env.VITE_EMAILJS_PUBLIC_KEY;

    console.log(serviceId, templateId, publicKey);

    const result = await emailjs.send(
      serviceId,
      templateId,
      {
        nom: nom.value,
        email: email.value,
        message: message.value,
      },
      publicKey
    );

    // Vider le formulaire
    resetForm();
    dialog.value = false;
  } catch (error) {
    alert('Erreur lors de l’envoi : ' + error.text);
  }
});
</script>

<template>
  <footer class="footer">
    <span>© 2025</span> |
    <a href="#" @click.prevent="dialog = true" class="contact-link">Me contacter</a>

    <v-dialog v-model="dialog" max-width="600">
      <v-card>
        <v-card-title class="text-h5">Contactez-moi</v-card-title>
        <v-card-text>
          <v-form @submit.prevent="sendForm">
            <v-text-field v-model="nom" label="Nom" :error-messages="errors.nom" required />
            <v-text-field v-model="email" label="Email" type="email" :error-messages="errors.email" required />
            <v-textarea v-model="message" label="Message" :error-messages="errors.message" rows="4" required />
            <v-card-actions class="justify-end">
              <v-btn color="primary" type="submit">Envoyer</v-btn>
              <v-btn text @click="dialog = false">Annuler</v-btn>
            </v-card-actions>
          </v-form>
        </v-card-text>
      </v-card>
    </v-dialog>
  </footer>
</template>

<style scoped>
.footer {
  text-align: center;
  margin-top: 60px;
  padding: 20px;
  background-color: silver;
  color: var(--vt-c-white);
  font-size: 14px;
}
.contact-link {
  color: var(--vt-c-custom-text-2);
  margin-left: 10px;
  text-decoration: underline;
  cursor: pointer;
}
.contact-link:hover {
  color: var(--vt-c-custom-text-1);
}
</style>
