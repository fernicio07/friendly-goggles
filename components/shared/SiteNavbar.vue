<template>
  <nav class="top-nav">
    <div class="logo">
      <img alt="logo" src="../../assets/img/logo.png" />
    </div>
    <ul>
      <li>Home</li>
      <li>Uno</li>
      <li>Dos</li>
      <li>Tres</li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #ccc;
  padding: 0 2rem;
  
  .logo {
    padding: 1rem 0;
  }

  ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;

    li {
      background-image: linear-gradient(#02daff, #0bb2f5);
      border: 1px solid #808080;
      padding: 0.75rem;
      text-decoration: none;
      color: white;
    }
  }
}

@media screen and (max-width: 375px) {
  .top-nav {
    flex-direction: column;
    
    ul {
      margin: 1rem 0;
    }
  }
}
</style>
