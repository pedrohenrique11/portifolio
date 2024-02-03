<script>

</script>

<template>
    <div class="content">
        <img src="./imgs/room-265x265.gif" alt="">
        <div class="text-section">
            <p class="who">Who i am?</p>
            <h3 class="profile-title">Pedro Henrique</h3>
            <p class="profile-subtitle">Front-end Developer</p>
            <p class="profile-text">I've always been captivated by how technology is capable of changing people's lives, helping with everyday or more important issues. With this in mind, I started studying programming with the intention of creating something, something that could help in some way. I'm currently studying at EBAC, where I'm specializing as a JavaScript developer and its freamworks like Vue.js and React.Come check out some of the projects!</p>
        </div>
    </div>
</template>

<style scoped>
  .content {
    display: flex;
    justify-content: space-between;
    padding: 1rem;
    margin: 15rem auto;

    border-radius: 3px;
    border: 1px solid var(--primary-dark-color);
    background-color: var(--primary-dark-color);

    transition: border .5s ease;
  }
  .content:hover {
    border: 1px solid var(--secondary-color);
  }
  img {
    width: 22rem;
    height: 22rem;
    margin: auto;

    border-radius: 3px;
  }
  .text-section {
    padding: 0 2rem;
  }
  .profile-title {
    font-size: 2rem;
    color: #fff;
  }
  .profile-subtitle {
    color: var(--secondary-color);
    margin-bottom: 1rem;
  }

  @media (max-width: 800px){
    .content {
        flex-direction: column;
    }
    img {
        width: 24rem;
        margin-bottom: 1rem;
    }
    .text-section {
    padding: 1rem 0;
  }
  }
</style>