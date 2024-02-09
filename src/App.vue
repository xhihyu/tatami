<template>
  <div class="container">
    <div v-if="showButtonsAndImage">
      <div><img src="./assets/Cartoon-love-gif.gif" alt=""></div>
      <h1 class="title">Dear tata, will you be my valentine?</h1>
      <div class="button-container">
        <button @click="handleYesClick" :style="{ fontSize: yesButtonSize + 'px' }" class="button">Yes</button>
        <button @click="handleNoClick" class="button">No</button>
      </div>
    </div>
    <div v-else>
      <img v-if="currentImage === 'envelope'" src="./assets/Love-Letter-Envelope-Graphics-25185593-1.png" alt="Love Letter Envelope" @click="handleImageClick">
      <img v-else class="small-img" src="./assets/IMG_0011.png" alt="IMG 0011" @click="handleImageClick">
    </div>
  </div>
</template>

<script>
import sound from "./assets/Elvis Presley - Can't Help Falling in Love (Lyrics).mp3"
export default {
  data() {
    return {
      yesButtonSize: 16, // Initial size of the "Yes" button
      showButtonsAndImage: true, // Whether to show buttons and image
      currentImage: 'envelope' // Currently displayed image
    };
  },
  methods: {
    handleYesClick() {
      // Handle Yes button click
      const audio = new Audio(sound);
      audio.play();
      // Hide buttons and image after "Yes" clicked
      this.showButtonsAndImage = false;
    },
    handleNoClick() {
      // Handle No button click
      this.yesButtonSize += 2; // Increase the size of the "Yes" button
    },
    handleImageClick() {
  // Change the currently displayed image when clicked
  this.currentImage = 'IMG_0011';
  alert('Hey baby, thank you for coming into my life :) I am really glad that I met you, and have the opportunity to talk to you and know you! I really hope that we will be able to stay so loving and happy like this, and I hope that you are able to feel my love all the time, even through a ldr. I saw a quote that makes a lot of sense, distance means so little when you mean so much to me! I will work hard and make lots of money so we can live a comfortable life together next time! I hope I can be an important person in your life, and you are so so so important to me! I will cherish you, and take care of you, and I will never ever break your heart <3 I am so excited to see you and I love you so much baby !!!  ');
}

  }
};
</script>

<style scoped>
/* Center content vertically and horizontally */
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-image: url('./assets/Cute-Tiny-Heart-Pattern-Floating-Up-Animated-Gif.gif');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

/* Apply "Great Vibes" font to the title */
.title {
  font-family: 'Great Vibes', cursive;
}

/* Center buttons horizontally */
.button-container {
  margin-top: 20px;
  text-align: center; /* Center-align buttons */
}

.button {
  font-family: 'Great Vibes', cursive;
  background-color: #FF4081;
  color: #FFFFFF;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  margin-right: 10px;
  cursor: pointer;
}

.button:hover {
  background-color: #D81B60;
}

/* Style for smaller image */
.small-img {
  max-width: 500px; /* Adjust the width as needed */
  height: auto;
}
</style>
