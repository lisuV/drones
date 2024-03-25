<script>
export default {
  data() {
    return {
      showMessage: false,
      messageText: '',
      firstName: '',
      email: '',
      message: ''
    }
  },
  methods: {
    sendContactForm() {
      console.log({
        firstName: this.firstName,
        email: this.email,
        message: this.message
      })
      this.firstName = ''
      this.email = ''
      this.message = ''
      this.showMessage = true
      this.messageText = 'Message was successfully sent!'
      /*setTimeout(() => {
        this.showMessage = false
        this.messageText = ''
      }, 5000)*/
    }
  }
}
</script>
<template>
  <main>
    <div class="slide">
      <h1 class="main-header">Contact us</h1>
      <form @submit.prevent="sendContactForm" class="form-container">
        <div class="input-group">
          <input
            v-model="firstName"
            id="firstName"
            name="firstName"
            type="text"
            required
            class="input-field"
            placeholder="First and Last Name"
          />
        </div>
        <div class="input-group">
          <input
            v-model="email"
            id="email"
            name="email"
            type="email"
            required
            class="input-field"
            placeholder="Email"
          />
        </div>
        <div class="input-group">
          <textarea
            v-model="message"
            id="message"
            name="message"
            required
            class="input-field"
            placeholder="Comment or Message"
          ></textarea>
        </div>
        <button type="submit" class="submit-button">Submit</button>
      </form>
    </div>
    <div v-if="showMessage" class="message">
      {{ messageText }}
    </div>
  </main>
</template>

<style>
.main {
  background: #f9f9f9;
}

.main-header {
  color: #121212;
  font-family: 'Montserrat', sans-serif;
  font-size: 48px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

.slide {
  margin-top: 190px;
  display: flex;
  flex-direction: column;
  align-items: center;
  flex-wrap: wrap;
  width: -webkit-fill-available;
}

.form-container {
  padding-top: 65px;
  margin-bottom: 135px;
  display: flex;
  flex-direction: column;
  align-items: start;
  width: -webkit-fill-available;
  gap: 24px;
  margin-left: 6.6%;
  margin-right: 6.6%;
}
.input-group {
  width: 100%;
}

.input-field {
  border-radius: 8px;
  border: 1px solid rgba(18, 18, 18, 0.8);
  padding: 10px 10px 10px 10px;
  width: 35%;
  color: #121212;
  font-family: 'Montserrat', sans-serif;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

.input-field:focus {
  outline: none;
  border-color: #4caf50;
}

.input-field::placeholder {
  color: #adadad;
  font-family: 'Montserrat', sans-serif;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

textarea.input-field {
  height: 160px;
  resize: none;
  width: 47%;
}

button {
  display: inline-flex;
  padding: 14px 18px;
  justify-content: center;
  align-items: center;
  gap: 10px;

  border-radius: 8px;
  background: #121212;

  color: #fff;
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

.message {
  background-color: #4caf50;
  color: #fff;
  padding: 10px;
  border-radius: 5px;
}
</style>
