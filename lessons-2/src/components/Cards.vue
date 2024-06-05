<template>
  <div>
    <h2>Повідомлення {{ message }}</h2>
    <form @submit.prevent="submitForm">
      <label for="name">Name:</label>
      <input type="text" id="name" v-model="name" />
      <label for="email">Email:</label>
      <input type="email" id="email" v-model="email" />
      <button type="submit">Submit</button>
    </form>
    <ul v-if="submissions.length > 0">
      <li v-for="(submission, index) in submissions" :key="index">
        <h3>Ім'я: {{ submission.name }}</h3>
        <h3>Пошта: {{ submission.email }}</h3>
        <button @click="deleteSubmission(index)">Delete</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      submissions: [],
    };
  },
  methods: {
    submitForm() {
      const newSubmission = {
        name: this.name,
        email: this.email,
      };
      this.submissions.push(newSubmission);
      this.name = "";
      this.email = "";
    },
    deleteSubmission(index) {
      this.submissions.splice(index, 1);
    },
  },
  computed: {
    message() {
      const count = this.submissions.length;
      if (count === 0) {
        return "Вибачте, ще немає повідомлень!";
      } else if (count === 1) {
        return "1 повідомлення";
      } else {
        return `${count} повідомлень`;
      }
    },
  },
};
</script>

<style></style>
