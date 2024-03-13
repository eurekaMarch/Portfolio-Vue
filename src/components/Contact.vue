<template>
  <section class="contact container section" id="contact">
    <h2 class="section__title">Get In Touch</h2>

    <div class="contact__container grid">
      <div class="contact__info">
        <h3 class="contact__title">Let's talk about everything!</h3>
        <p class="contact__details">Don't like forms? Send me an email. 👋</p>
      </div>

      <form action="" class="contact__form">
        <div class="contact__form--group">
          <div class="contact__form--div">
            <input
              type="text"
              placeholder="Insert your name"
              class="contact__form--input"
            />
          </div>

          <div class="contact__form--div">
            <input
              type="text"
              placeholder="Insert your email"
              class="contact__form--input"
            />
          </div>
        </div>

        <div class="contact__form--div">
          <input
            type="text"
            placeholder="Insert your subject"
            class="contact__form--input"
          />
        </div>

        <textarea
          name=""
          id=""
          cols="30"
          rows="10"
          placeholder="Write your message"
          class="contact__form--div contact__form--input contact__form--area"
        ></textarea>

        <button class="btn">Send Message</button>
      </form>
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
.contact.section {
  padding-bottom: 6.25rem;
}

.contact__container {
  grid-template-columns: 4fr 8fr;
  column-gap: 1.875rem;
}

.contact__title {
  font-size: var(--h3-font-size);
  margin-bottom: 0.5rem;
}

.contact__form--group {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  column-gap: 1.5rem;
}

.contact__form--div {
  margin-bottom: 1.875rem;
  height: 3.75rem;
}

.contact__form--input {
  width: 100%;
  height: 100%;
  box-shadow: var(--shadow);
  background-color: var(--container-color);
  color: var(--text-color);
  border: none;
  outline: none;
  border-radius: 1.875rem;
  padding: 0.625rem 1.875rem;
  z-index: 1;
}

.contact__form--area {
  height: 10.25rem;
}
</style>
