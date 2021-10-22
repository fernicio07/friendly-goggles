<template>
  <div class="footer">
    <div class="footer-nav">
      <p>© Copyright, All Rights Reserved.</p>
      <ul>
        <li>Home</li>
        <li>Uno</li>
        <li>Dos</li>
        <li>Tres</li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.footer {
  background-color: #ccc;
  padding: 2rem;

  .footer-nav {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;

    ul {
      list-style-type: none;
      display: flex;

      li {
        margin-right: 0.875rem;

        &:not(:last-child) {
          padding-right: 0.75rem;
          border-right: 1px solid;
        }
      }
    }
  }
}

@media screen and (max-width: 375px) {
  .footer-nav {
    align-items: center;
    flex-direction: column;
  }
}
</style>
