<template>
  <Transition name="fade" mode="out-in" appear>
    <div v-if="!isForm" class="hello-parent flex flex-col" key="Hello">
      <svg class="hello-word" width="365" height="277" viewBox="0 0 365 277">
        <g id="H-letter">
          <line
            class="H-left-stroke"
            x1="17"
            y1="17"
            x2="17"
            y2="104"
            stroke="#fff"
            fill="none"
            stroke-width="34"
            stroke-linecap="round"
          />
          <line
            class="H-mid-stroke"
            x1="17"
            y1="17"
            x2="82"
            y2="17"
            stroke="#fff"
            fill="none"
            stroke-width="34"
            stroke-linecap="round"
          />
          <line
            class="H-mid-stroke-delayed"
            x1="17"
            y1="62"
            x2="82"
            y2="62"
            stroke="#fff"
            fill="none"
            stroke-width="34"
            stroke-linecap="round"
          />
          <line
            class="H-right-stroke"
            x1="84"
            y1="17"
            x2="84"
            y2="104"
            stroke="#fff"
            fill="none"
            stroke-width="34"
            stroke-linecap="round"
          />
        </g>
        <g id="I-letter">
          <!-- <circle class="O-stroke-i" cx="138" cy="20" r="5" stroke="#fff" fill="none" stroke-width="20" /> -->
          <line
            class="I-letter"
            x1="138"
            y1="62"
            x2="138"
            y2="104"
            stroke="#fff"
            fill="none"
            stroke-width="34"
            stroke-linecap="round"
          />
        </g>

        <!-- <g id="E-letter">
        <line class="E-left-stroke" x1="138" y1="0" x2="138" y2="124" stroke="#000" fill="none" stroke-width="34" />
        <line class="E-top-stroke" x1="154" y1="17" x2="201" y2="17" stroke="#000" fill="none" stroke-width="34" />
        <line class="E-mid-stroke" x1="154" y1="62" x2="196" y2="62" stroke="#000" fill="none" stroke-width="34" />
        <line class="E-bottom-stroke" x1="154" y1="107" x2="201" y2="107" stroke="#000" fill="none" stroke-width="34" />
      </g> -->

        <g id="L-one-letter">
          <line
            class="L-one-long-stroke"
            x1="17"
            y1="170"
            x2="17"
            y2="260"
            stroke="#fff"
            fill="none"
            stroke-width="34"
          />
          <line
            class="L-one-short-stroke"
            x1="20"
            y1="170"
            x2="84"
            y2="260"
            stroke="#fff"
            fill="none"
            stroke-width="34"
            stroke-linecap="round"
          />
          <line
            class="L-one-long-stroke"
            x1="84"
            y1="170"
            x2="84"
            y2="260"
            stroke="#fff"
            fill="none"
            stroke-width="34"
          />
        </g>

        <g id="L-two-letter">
          <line
            class="L-two-long-stroke"
            x1="138"
            y1="170"
            x2="138"
            y2="260"
            stroke="#fff"
            fill="none"
            stroke-width="34"
            stroke-linecap="round"
          />
          <line
            class="L-two-long-stroke-delayed"
            x1="205"
            y1="170"
            x2="205"
            y2="260"
            stroke="#fff"
            fill="none"
            stroke-width="34"
            stroke-linecap="round"
          />
          <line
            class="L-two-short-stroke"
            x1="140"
            y1="260"
            x2="200"
            y2="260"
            stroke="#fff"
            fill="none"
            stroke-width="34"
            stroke-linecap="round"
          />
        </g>

        <!-- <g id="O-letter">
        <circle class="O-stroke" cx="231" cy="215" r="48" stroke="#fff" fill="none" stroke-width="31" />
      </g> -->
        <g id="R-letter">
          <line
            class="R-two-long-stroke"
            x1="264"
            y1="153"
            x2="264"
            y2="274"
            stroke="#fff"
            stroke-width="34"
          ></line>
          <line
            class="R-long-stroke"
            x1="331"
            y1="170"
            x2="331"
            y2="213"
            stroke="#fff"
            stroke-width="34"
          ></line>
          <line
            class="R-long-stroke"
            x1="331"
            y1="231"
            x2="331"
            y2="274"
            stroke="#fff"
            stroke-width="34"
          ></line>
          <line
            class="H-mid-stroke-delayed"
            x1="264"
            y1="214"
            x2="315"
            y2="214"
            stroke="#fff"
            fill="none"
            stroke-width="34"
          />
          <line
            class="H-mid-stroke-delayed"
            x1="264"
            y1="170"
            x2="315"
            y2="170"
            stroke="#fff"
            fill="none"
            stroke-width="34"
          />
        </g>

        <g id="red-dot">
          <line
            x1="138"
            y1="20"
            x2="138"
            y2="20"
            stroke="#ff003c"
            class="red-dot"
          />
        </g>
        <g id="green-dot">
          <line
            x1="138"
            y1="20"
            x2="138"
            y2="20"
            stroke="#00ff48"
            stroke-width="33"
            class="green-dot"
          />
        </g>
        <g id="blue-dot">
          <line
            x1="138"
            y1="20"
            x2="138"
            y2="20"
            stroke="#0055ff"
            stroke-width="33"
            class="blue-dot"
          />
        </g>
        <g id="yellow-dot">
          <line
            x1="138"
            y1="20"
            x2="138"
            y2="20"
            stroke="#f9f942"
            stroke-width="33"
            class="yellow-dot"
          />
        </g>
      </svg>
      <p class="text-white tracking-[0.3rem] text-lg pt-4 mount-anime pointer-events-none">
        Web-developer / Freelancer
      </p>
    </div>
    <div
      v-else
      id="sheet"
      class="bg-white bg-opacity-0 w-[365px] h-[321px] pb-4 grid grid-cols-2 grid-rows-[1fr_1fr_3fr_1fr] gap-3 place-items-center relative"
    >
      <div class="form mount-anime-name z-10">
        <input
          v-model="nameValue"
          maxlength="15"
          type="text"
          name="text"
          autocomplete="off"
          required
        />
        <label for="text" class="label-name">
          <span class="content-name"> Имя </span>
        </label>
      </div>
      <div class="form mount-anime-subject z-10">
        <input
          v-model="subjectValue"
          maxlength="18"
          type="text"
          name="text"
          autocomplete="off"
          required
        />
        <label for="text" class="label-name">
          <span class="content-name"> Тема сообщения </span>
        </label>
      </div>
      <div class="form mount-anime-mail col-span-2">
        <input
          v-model="emailValue"
          type="text"
          name="text"
          maxlength="30"
          autocomplete="off"
          required
        />
        <label for="text" class="label-name">
          <span class="content-name"> Почта </span>
        </label>
      </div>
      <div
        class="form mount-anime-textarea row-start-3 row-end-4 col-start-1 col-end-3"
      >
        <textarea
          v-model="textareaValue"
          maxlength="200"
          spellcheck="false"
          placeholder="Сообщение"
          type="text"
          name="text"
          autocomplete="off"
          required
          class=" max-md:text-[16px]"
        ></textarea>
        <label for="text" class="label-name">
          <!-- <span class="content-name"> Содержание </span> -->
        </label>
      </div>

      <button
        @click="sendForm()"
        class="row-start-4 row-end-5 col-start-1 col-end-3 bg-sky-500 bg-opacity-1 transition-all w-[100%] mount-anime-send rounded-[0.5rem] text-white hover:bg-sky-700"
      >
        Отправить
      </button>
      <div
        id="bot"
        class="bg-white bg-opacity-0 absolute w-[80%] h-[3.7rem] right-2 top-0 z-0 bot-animation grid grid-cols-[4fr_1fr]"
      >
        <div
          id="messagebox"
          class="bg-white h-10 message-borders w-[95%] flex items-center bot-message-anime"
        >
          <p class="px-2 leading-[1rem]">{{ botResponse }}</p>
        </div>
        <img
          src="../images/bot.png"
          alt="Bot"
          class="object-contain w-[100%] col-start-2 col-end-3"
        />
      </div>
    </div>
  </Transition>
  <button
    class="button-64 mount-anime-btn mt-4"
    role="button"
    @click="changeState"
  >
    <span class="text">{{ btnState }}</span>
  </button>
</template>

<script lang="ts">
import axios from "axios";

export default {
  data() {
    return {
      // isBot: false,
      isForm: false,
      nameValue: "",
      subjectValue: "",
      emailValue: "",
      textareaValue: "",
      isSendButtonClicked: false,
      botResponse: "Привет, я помогу тебе заполнить форму, бип.",
    };
  },
  methods: {
    changeState(): void {
      this.isForm = !this.isForm;
    },
    inputClean() {
      this.nameValue = "";
      this.subjectValue = "";
      this.emailValue = "";
      this.textareaValue = "";
    },
    changeSendButtonState() {
      if (!this.isSendButtonClicked) {
        this.isSendButtonClicked = !this.isSendButtonClicked;
        // setTimeout(() => {
        //   this.isSendButtonClicked = !this.isSendButtonClicked;
        // }, 1000);
      }
    },
    async sendRequest() {
      try {
        const options = {
          method: "POST",
          url: "https://api.telegram.org/bot5847470412%3AAAHs4sky2p9-PFyrz7v98nhCTRoYLRm6rSM/sendMessage",
          headers: {
            accept: "application/json",
            "content-type": "application/json",
          },
          data: {
            text: `<b>Name:</b>\n${this.nameValue}\n<b>Subject:</b>\n${this.subjectValue}\n<b>Email:</b>\n${this.emailValue}\n<b>Text:</b>\n${this.textareaValue}`,
            disable_web_page_preview: false,
            disable_notification: false,
            parse_mode: "HTML",
            reply_to_message_id: null,
            chat_id: "602753868",
          },
        };

        await axios.request(options);
        this.inputClean();
      } catch (error) {
        console.log(error);
        this.botResponse = "Что-то сломалось! Проверь интернет.";
      }
    },
    botResponseOptions() {
      const emailCheck = this.emailValue.split("@").length;
      if (
        this.nameValue &&
        this.textareaValue &&
        this.subjectValue &&
        emailCheck !== 2 &&
        this.isSendButtonClicked
      )
        return "Попробуй формат почты example@index.ru";
      else if (
        this.nameValue &&
        this.textareaValue &&
        this.subjectValue &&
        emailCheck === 2 &&
        this.isSendButtonClicked
      )
        return "Готово! Я отправил все создателю.";
      return "Заполни все поля.";
    },
    check() {
      console.log(this.nameValue);
      console.log(this.subjectValue);
      const emailCheck = this.emailValue.split("@").length;
      console.log(this.emailValue);
      console.log(emailCheck);
      console.log(this.textareaValue);
    },
    sendForm() {
      this.changeSendButtonState();
      this.botResponse = this.botResponseOptions();
      const emailCheck = this.emailValue.split("@").length;
      if (
        emailCheck === 2 &&
        this.nameValue &&
        this.textareaValue &&
        this.subjectValue
      ) {
        this.sendRequest();
      }
    },
  },
  computed: {
    btnState() {
      return this.isForm ? "Вернуться" : "Напиши мне";
    },
  },
};
</script>

<style scoped>
html,
body,
.hello-parent {
  height: 100%;
  width: 100%;
  margin: 0;
}

*, *::after, *::before {
  -webkit-user-select: none;
     -moz-user-select: none;
      -ms-user-select: none;
          user-select: none;
}

.message-borders {
  border-radius: 1rem 1rem 0 1rem;
}

.bot-animation {
  transform: translateY(-3.4rem);
  -webkit-animation: bot-move 10s ease;
          animation: bot-move 10s ease;
}

@-webkit-keyframes bot-move {
  0% {
    opacity: 0;
    transform: translateY(0);
  }
  30% {
    opacity: 0;
    transform: translateY(0);
  }
  40% {
    transform: translateY(-3.4rem);
    opacity: 1;
  }
  50% {
  }
  100% {
    transform: translateY(-3.4rem);
  }
}

@keyframes bot-move {
  0% {
    opacity: 0;
    transform: translateY(0);
  }
  30% {
    opacity: 0;
    transform: translateY(0);
  }
  40% {
    transform: translateY(-3.4rem);
    opacity: 1;
  }
  50% {
  }
  100% {
    transform: translateY(-3.4rem);
  }
}

.bot-message-anime {
  /* transform: translateX(100px) translateY(15px) scale(10%) ; */
  transition-property: all;
  /* transition: 1s ease; */
  -webkit-animation: bot-message-move 10s ease;
          animation: bot-message-move 10s ease;
  /* width: 95%; */
}

@-webkit-keyframes bot-message-move {
  0% {
    opacity: 0;
  }
  40% {
    opacity: 0;
    transform: translateX(100px) translateY(15px) scale(10%);
  }
  45% {
    opacity: 1;
    transform: translateX(0) translateY(0) scale(100%);
  }
}

@keyframes bot-message-move {
  0% {
    opacity: 0;
  }
  40% {
    opacity: 0;
    transform: translateX(100px) translateY(15px) scale(10%);
  }
  45% {
    opacity: 1;
    transform: translateX(0) translateY(0) scale(100%);
  }
}

.form {
  width: 100%;
  position: relative;
  height: 60px;
  overflow: hidden;
  border-radius: 0.5rem;
}

.form:nth-child(4) {
  height: 100%;
}

.form input,
.form textarea {
  width: 100%;
  height: 100%;
  color: #fff;
  padding-top: 20px;
  border: none;
  background-color: #484848;
  text-indent: 0.3rem;
}

.form textarea {
  padding-top: 0.2rem;
  line-height: 1rem;
  padding-left: 0.2rem;
  font-size: small;
  resize: none;
}

@media (max-width: 768px) {
  .form textarea {
  font-size: 16px;
  }
}

.form label {
  position: absolute;
  bottom: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  pointer-events: none;
  /* border-bottom: 1px solid white; */
}
.form label::after {
  content: "";
  position: absolute;
  bottom: -1px;
  left: 0px;
  width: 100%;
  height: 100%;
  border-bottom: 4px solid;
  -o-border-image: linear-gradient(
      to right,
      #00ff48 0%,
      #f9f942 25%,
      #ff003c 50%,
      #0055ff 90%
    )
    5;
     border-image: linear-gradient(
      to right,
      #00ff48 0%,
      #f9f942 25%,
      #ff003c 50%,
      #0055ff 90%
    )
    5;
  transform: translateX(-100%);
  transition: all 0.3s ease;
}

.content-name {
  position: absolute;
  bottom: 0px;
  left: 0.5rem;
  padding-bottom: 5px;
  transition: all 0.4s ease;
  color: white;
}
.form input:focus {
  outline: none;
}
.form textarea:focus {
  outline: none;
}
.form input:focus + .label-name .content-name,
.form input:valid + .label-name .content-name {
  transform: translateY(-130%);
  font-size: 14px;
  left: 0.3rem;
  color: #fff;
}

/* .form input:invalid + .label-name .content-name {
  transform: translateY(-130%);
  font-size: 14px;
  left: 0.3rem;
  color: #fff;
} */

.form textarea:focus + .label-name .content-name,
.form textarea:valid + .label-name .content-name {
  transform: translateY(-130%);
  font-size: 14px;
  left: 0.3rem;
  color: #fff;
}
.form input:focus + .label-name::after,
.form input:valid + .label-name::after {
  transform: translateX(0%);
}

.form textarea:focus + .label-name::after,
.form textarea:valid + .label-name::after {
  transform: translateX(0%);
}

.fade-enter-active {
  transition: opacity 1s ease;
}

.fade-leave-active {
  transition: opacity 1s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.button-64 {
  align-items: center;
  background-image: linear-gradient(
    144deg,
    #00ff48,
    #f9f942 30%,
    #ff003c 60%,
    #0055ff
  );
  border: 0;
  border-radius: 17px;
  /* box-shadow: rgba(151, 65, 252, 0.2) 0 15px 30px -5px; */
  box-sizing: border-box;
  color: #ffffff;
  display: flex;
  /* font-family: Phantomsans, sans-serif; */
  font-size: 20px;
  justify-content: center;
  line-height: 0.8rem;
  max-width: 10rem;
  min-width: 140px;
  padding: 3px;
  text-decoration: none;
  -moz-user-select: none;
   -ms-user-select: none;
       user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  white-space: nowrap;
  cursor: pointer;
}

.button-64:active,
.button-64:hover {
  outline: 0;
  color: #000;
}

.button-64 span {
  background-color: rgb(0, 0, 0);
  padding: 16px 24px;
  border-radius: 17px;
  width: 100%;
  height: 100%;
  transition: 300ms;
}

.button-64:hover span {
  background: none;
}

@media (min-width: 768px) {
  .button-64 {
    font-size: 24px;
    min-width: 196px;
  }
}
.mount-anime-name {
  /* animation-delay: 3s; */
  opacity: 1;
  -webkit-animation: mount-move 1.5s ease;
          animation: mount-move 1.5s ease;
}
.mount-anime-subject {
  /* animation-delay: 3s; */
  opacity: 1;
  -webkit-animation: mount-move 1.7s ease;
          animation: mount-move 1.7s ease;
}
.mount-anime-mail {
  /* animation-delay: 3s; */
  opacity: 1;
  -webkit-animation: mount-move 2s ease;
          animation: mount-move 2s ease;
}
.mount-anime-textarea {
  /* animation-delay: 3s; */
  opacity: 1;
  -webkit-animation: mount-move 2.2s ease;
          animation: mount-move 2.2s ease;
}

.mount-anime-send {
  /* animation-delay: 3s; */
  opacity: 1;
  -webkit-animation: mount-move 2.5s ease;
          animation: mount-move 2.5s ease;
}

.mount-anime-btn {
  /* opacity: 1; */
  -webkit-animation: mount-move 4s ease;
          animation: mount-move 4s ease;
}

@-webkit-keyframes mount-move {
  0% {
    transform: translateY(40px);
    opacity: 0;
  }

  40% {
    transform: translateY(40px);
    opacity: 0;
  }
  60% {
    /* transform: translateY(5px); */
    opacity: 1;
  }
  100% {
    opacity: 1;
  }
}

@keyframes mount-move {
  0% {
    transform: translateY(40px);
    opacity: 0;
  }

  40% {
    transform: translateY(40px);
    opacity: 0;
  }
  60% {
    /* transform: translateY(5px); */
    opacity: 1;
  }
  100% {
    opacity: 1;
  }
}

.hello-parent {
  background: rgb(0, 0, 0);
  /* background: -webkit-radial-gradient(#fff, #eaeaea);
  background: -o-radial-gradient(#fff, #eaeaea);
  background: -moz-radial-gradient(#fff, #eaeaea);
  background: radial-gradient(#fff, #eaeaea); */
}

.hello-word {
  /* position: absolute; */
  margin: auto;
  background-color: rgb(0, 0, 0);
  /* border: #fff 1px solid; */
}
/* H Animation */

.H-left-stroke {
  stroke-dasharray: 87px;
  /* stroke-dashoffset: 124; */
  -webkit-animation: H-left-move 20s ease forwards;
          animation: H-left-move 20s ease forwards;
}

.H-mid-stroke-delayed {
  stroke-dasharray: 67px;
  stroke-dashoffset: 67px;
  -webkit-animation: H-mid-move 20s ease forwards;
          animation: H-mid-move 20s ease forwards;
  -webkit-animation-delay: 0.5s;
          animation-delay: 0.5s;
}
.H-mid-stroke {
  stroke-dasharray: 67px;
  stroke-dashoffset: 67px;
  -webkit-animation: H-mid-move 20s ease forwards;
          animation: H-mid-move 20s ease forwards;
}

.H-right-stroke {
  stroke-dasharray: 87px;
  stroke-dashoffset: 104px;
  -webkit-animation: H-right-move 20s ease forwards;
          animation: H-right-move 20s ease forwards;
}

@-webkit-keyframes H-left-move {
  0% {
    stroke-dashoffset: 87px;
  }
  5% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes H-left-move {
  0% {
    stroke-dashoffset: 87px;
  }
  5% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@-webkit-keyframes H-mid-move {
  0% {
    stroke-dashoffset: 67px;
  }
  5% {
    stroke-dashoffset: 67px;
  }
  10% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes H-mid-move {
  0% {
    stroke-dashoffset: 67px;
  }
  5% {
    stroke-dashoffset: 67px;
  }
  10% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@-webkit-keyframes H-right-move {
  0% {
    stroke-dashoffset: 87px;
  }
  5% {
    stroke-dashoffset: 87px;
  }
  10% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes H-right-move {
  0% {
    stroke-dashoffset: 87px;
  }
  5% {
    stroke-dashoffset: 87px;
  }
  10% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

/* E Animation */

.E-left-stroke {
  stroke-dasharray: 124px;
  stroke-dashoffset: 124px;
  -webkit-animation: E-left-move 20s ease forwards;
          animation: E-left-move 20s ease forwards;
}

.E-top-stroke {
  stroke-dasharray: 47px;
  stroke-dashoffset: 47px;
  -webkit-animation: E-top-move 10s ease forwards;
          animation: E-top-move 10s ease forwards;
}

.E-mid-stroke {
  stroke-dasharray: 42px;
  stroke-dashoffset: 42px;
  -webkit-animation: E-mid-move 10s ease forwards;
          animation: E-mid-move 10s ease forwards;
}

.E-bottom-stroke {
  stroke-dasharray: 47px;
  stroke-dashoffset: 47px;
  -webkit-animation: E-bottom-move 10s ease forwards;
          animation: E-bottom-move 10s ease forwards;
}

@-webkit-keyframes E-left-move {
  0% {
    stroke-dashoffset: 124px;
  }
  2% {
    stroke-dashoffset: 124px;
  }
  6% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes E-left-move {
  0% {
    stroke-dashoffset: 124px;
  }
  2% {
    stroke-dashoffset: 124px;
  }
  6% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@-webkit-keyframes E-top-move {
  0% {
    stroke-dashoffset: 47px;
  }
  6% {
    stroke-dashoffset: 47px;
  }
  11% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes E-top-move {
  0% {
    stroke-dashoffset: 47px;
  }
  6% {
    stroke-dashoffset: 47px;
  }
  11% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@-webkit-keyframes E-mid-move {
  0% {
    stroke-dashoffset: 42px;
  }
  8% {
    stroke-dashoffset: 42px;
  }
  13% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes E-mid-move {
  0% {
    stroke-dashoffset: 42px;
  }
  8% {
    stroke-dashoffset: 42px;
  }
  13% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@-webkit-keyframes E-bottom-move {
  0% {
    stroke-dashoffset: 47px;
  }
  11% {
    stroke-dashoffset: 47px;
  }
  16% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes E-bottom-move {
  0% {
    stroke-dashoffset: 47px;
  }
  11% {
    stroke-dashoffset: 47px;
  }
  16% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

/* L One Animation */

.L-one-long-stroke {
  /* border-radius: 50px; */
  stroke-dasharray: 90px;
  stroke-dashoffset: 90px;
  stroke-linecap: round;
  -webkit-animation: L-one-long-move 50s ease forwards;
          animation: L-one-long-move 50s ease forwards;
}

.L-one-short-stroke {
  stroke-dasharray: 110px;
  stroke-dashoffset: 110px;
  -webkit-animation: L-one-short-move 10s ease forwards;
          animation: L-one-short-move 10s ease forwards;
}

@-webkit-keyframes L-one-long-move {
  0% {
    stroke-dashoffset: 87px;
  }
  2% {
    stroke-dashoffset: 0px;
  }
  7% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes L-one-long-move {
  0% {
    stroke-dashoffset: 87px;
  }
  2% {
    stroke-dashoffset: 0px;
  }
  7% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@-webkit-keyframes L-one-short-move {
  0% {
    stroke-dashoffset: 110px;
  }
  13% {
    stroke-dashoffset: 0px;
  }
  18% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes L-one-short-move {
  0% {
    stroke-dashoffset: 110px;
  }
  13% {
    stroke-dashoffset: 0px;
  }
  18% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

/* L Two Animation */

.L-two-long-stroke {
  stroke-dasharray: 90px;
  stroke-dashoffset: 90px;
  -webkit-animation: L-two-long-move 20s ease forwards;
          animation: L-two-long-move 20s ease forwards;
}

.R-two-long-stroke {
  stroke-dasharray: 121px;
  stroke-dashoffset: 121px;
  -webkit-animation: R-two-long-move 20s ease forwards;
          animation: R-two-long-move 20s ease forwards;
}

.L-two-long-stroke-delayed {
  stroke-dasharray: 90px;
  stroke-dashoffset: 90px;
  -webkit-animation: L-two-long-move 20s ease forwards;
          animation: L-two-long-move 20s ease forwards;
  -webkit-animation-delay: 0.3s;
          animation-delay: 0.3s;
}

.L-two-short-stroke {
  stroke-dasharray: 60px;
  stroke-dashoffset: 60px;
  -webkit-animation: L-two-short-move 10s ease forwards;
          animation: L-two-short-move 10s ease forwards;
}

@-webkit-keyframes L-two-long-move {
  0% {
    stroke-dashoffset: 90px;
  }
  3% {
    stroke-dashoffset: 90px;
  }
  8% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes L-two-long-move {
  0% {
    stroke-dashoffset: 90px;
  }
  3% {
    stroke-dashoffset: 90px;
  }
  8% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@-webkit-keyframes R-two-long-move {
  0% {
    stroke-dashoffset: 121px;
  }
  3% {
    stroke-dashoffset: 121px;
  }
  8% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes R-two-long-move {
  0% {
    stroke-dashoffset: 121px;
  }
  3% {
    stroke-dashoffset: 121px;
  }
  8% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@-webkit-keyframes L-two-short-move {
  0% {
    stroke-dashoffset: 60px;
  }
  15% {
    stroke-dashoffset: 60px;
  }
  20% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes L-two-short-move {
  0% {
    stroke-dashoffset: 60px;
  }
  15% {
    stroke-dashoffset: 60px;
  }
  20% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

/* O Animation */

.O-stroke {
  stroke-dasharray: 302px;
  stroke-dashoffset: 302px;
  -webkit-animation: O-move 20s ease forwards;
          animation: O-move 20s ease forwards;
}

.O-stroke-i {
  stroke-dasharray: 302px;
  stroke-dashoffset: 302px;
  -webkit-animation: O-move 50s ease forwards;
          animation: O-move 50s ease forwards;
}

@-webkit-keyframes O-move {
  0% {
    stroke-dashoffset: 302px;
  }
  4% {
    stroke-dashoffset: 302px;
  }
  9% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes O-move {
  0% {
    stroke-dashoffset: 302px;
  }
  4% {
    stroke-dashoffset: 302px;
  }
  9% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

/* Red Dot Animation */

.red-dot {
  stroke-width: 0px;
  stroke-linecap: round;
  -webkit-animation: red-dot-grow 8s ease-out forwards;
          animation: red-dot-grow 8s ease-out forwards;
  -webkit-animation-delay: 1s;
          animation-delay: 1s;
}

.green-dot {
  stroke-width: 0px;
  stroke-linecap: round;
  -webkit-animation: green-dot-grow 8s ease-out forwards;
          animation: green-dot-grow 8s ease-out forwards;
  -webkit-animation-delay: 1.1s;
          animation-delay: 1.1s;
}

@-webkit-keyframes green-dot-grow {
  0% {
    stroke-width: 0px;
  }
  15% {
    stroke-width: 0px;
  }
  20% {
    stroke-width: 24px;
  }
  100% {
    stroke-width: 24px;
  }
}

@keyframes green-dot-grow {
  0% {
    stroke-width: 0px;
  }
  15% {
    stroke-width: 0px;
  }
  20% {
    stroke-width: 24px;
  }
  100% {
    stroke-width: 24px;
  }
}
.blue-dot {
  stroke-width: 0px;
  stroke-linecap: round;
  -webkit-animation: blue-dot-grow 8s ease-out forwards;
          animation: blue-dot-grow 8s ease-out forwards;
  -webkit-animation-delay: 1.2s;
          animation-delay: 1.2s;
}

@-webkit-keyframes blue-dot-grow {
  0% {
    stroke-width: 0px;
  }
  15% {
    stroke-width: 0px;
  }
  20% {
    stroke-width: 14px;
  }
  100% {
    stroke-width: 14px;
  }
}

@keyframes blue-dot-grow {
  0% {
    stroke-width: 0px;
  }
  15% {
    stroke-width: 0px;
  }
  20% {
    stroke-width: 14px;
  }
  100% {
    stroke-width: 14px;
  }
}
.yellow-dot {
  stroke-width: 0px;
  stroke-linecap: round;
  -webkit-animation: yellow-dot-grow 8s ease-out forwards;
          animation: yellow-dot-grow 8s ease-out forwards;
  -webkit-animation-delay: 1.3s;
          animation-delay: 1.3s;
}

@-webkit-keyframes yellow-dot-grow {
  0% {
    stroke-width: 0px;
  }
  15% {
    stroke-width: 0px;
  }
  20% {
    stroke-width: 4px;
  }
  100% {
    stroke-width: 4px;
  }
}

@keyframes yellow-dot-grow {
  0% {
    stroke-width: 0px;
  }
  15% {
    stroke-width: 0px;
  }
  20% {
    stroke-width: 4px;
  }
  100% {
    stroke-width: 4px;
  }
}

@-webkit-keyframes red-dot-grow {
  0% {
    stroke-width: 0px;
  }
  15% {
    stroke-width: 0px;
  }
  20% {
    stroke-width: 34px;
  }
  100% {
    stroke-width: 34px;
  }
}

@keyframes red-dot-grow {
  0% {
    stroke-width: 0px;
  }
  15% {
    stroke-width: 0px;
  }
  20% {
    stroke-width: 34px;
  }
  100% {
    stroke-width: 34px;
  }
}

.R-long-stroke {
  stroke-dasharray: 43px;
  stroke-dashoffset: 43px;
  -webkit-animation: r-two-stroke 2s ease forwards;
          animation: r-two-stroke 2s ease forwards;
}

@-webkit-keyframes r-two-stroke {
  0% {
    stroke-dashoffset: 43px;
  }
  80% {
    stroke-dashoffset: 10px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

@keyframes r-two-stroke {
  0% {
    stroke-dashoffset: 43px;
  }
  80% {
    stroke-dashoffset: 10px;
  }
  100% {
    stroke-dashoffset: 0px;
  }
}

.I-letter {
  stroke-dasharray: 42px;
  stroke-dashoffset: 42px;
  -webkit-animation: i-move 5s ease forwards;
          animation: i-move 5s ease forwards;
}

@-webkit-keyframes i-move {
  0% {
    stroke-dashoffset: 42px;
  }
  30% {
    stroke-dashoffset: 42px;
  }
  40% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0;
  }
}

@keyframes i-move {
  0% {
    stroke-dashoffset: 42px;
  }
  30% {
    stroke-dashoffset: 42px;
  }
  40% {
    stroke-dashoffset: 0px;
  }
  100% {
    stroke-dashoffset: 0;
  }
}

</style>
