<template lang="pug">
  div.blog
    h2 Страница "Блог"
    .blog-title Добавить запись
    .blog-row
      input(type='text' name='article-name' class='blog-input' placeholder="Название" required)
    .blog-row      
      input(type='text' name='article-date' class='blog-input' placeholder="Дата" required)  
    .blog-row      
      textarea(cols='30' rows='4' name='article-content' class='blog-text-area' placeholder="Содержание")   
    button(class="blog-save" type="button" @click="saveArticle") Добавить      
</template>
<script>
export default {
  methods: {
    saveArticle() {
      console.log('save all to JSON');
    }
  }
};
</script>

<style lang="scss">
.blog {
  position: relative;
}
.blog-row {
  position: relative;
  margin-top: 1.3rem;

  input {
    width: 80%;
    max-width: 25rem;
    padding: 0.5rem 1rem;
    border: none;
    outline: none;
    border-radius: 5px;
  }

  textarea {
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 5px;
    resize: none;
    overflow: hidden;
    outline: none;
    width: 100%;
    max-width: 35rem;
    height: 10rem;
  }
}
.blog-save {
  margin-top: 1.5rem;
  width: 119px;
  height: 46px;
  background-color: $green;
  border-radius: 5px;
  border: none;
  color: white;
  outline: none;

  &:hover {
    cursor: pointer;
  }
}
</style>
