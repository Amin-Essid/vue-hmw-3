<template>
  <div v-if="book !== null">
    <p>{{ book.title }}</p>
    <p>{{ book.author }}</p>
    <img
      v-if="book.isbn"
      v-bind:src="
        'http://covers.openlibrary.org/b/isbn/' + book.isbn + '-M.jpg'
      "
    />
    <p v-if="book.read">I have read this book</p>
    <p v-else>I have not read this book</p>
  </div>
</template>

<script>
export default {
  name: "BookDetails",
  props: {},
  data() {
    return {
      book: null,
    };
  },
  components: {},
  methods: {
    findBook() {
      for (const book of this.$store.state.books) {
        if (book.isbn === this.$route.params.isbn) {
          this.book = book;
        }
      }
    },
  },
  mounted() {
    this.findBook();
  },
};
</script>

<style></style>
