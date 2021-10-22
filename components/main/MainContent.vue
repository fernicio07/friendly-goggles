<template>
  <div class="min-h-screen bg-gray-100 sm:items-center sm:pt-0">
    <link
      href="https://cdn.jsdelivr.net/npm/tailwindcss@2.1.2/dist/tailwind.min.css"
      rel="stylesheet"
    />
    <div class="main-content">
      <div class="content-item">
        <h4>This is Some Content</h4>
        <img class="content-img" src="../../assets/img/column-left.jpg" />
        
        <p>
          Far far away, behind the word montains, far from the countries Vokalia
          and Consonantia, there live the blind texts. Separated they live in
          Bookmarksgrove right at the coast of the Semantics, a large language
          ocean.
        </p>
      </div>

      <div class="content-item">
        <h4>This is Some Content</h4>
        <img class="content-img" src="../../assets/img/column-center.jpg" />
        
        <ul>
          <li>
            <img src="../../assets/img/list.png" />
            Sed lacinia enim et nisl viverra.
          </li>
          
          <li>
            <img src="../../assets/img/list.png" /> 
            Nullam elementum quam in luctus.
          </li>
          
          <li>
            <img src="../../assets/img/list.png" /> 
            Integer ac et lacus hendrerit pretium.
          </li>
          
          <li>
            <img src="../../assets/img/list.png" /> 
            Donec placerat dui et blandit.
          </li>
          
          <li>
            <img src="../../assets/img/list.png" /> 
            Nullam elementum quam in luctus.
          </li>
        </ul>
      </div>

      <div class="content-item">
        <h4>What Others Are Saying</h4>
        <div
          v-for="testimonial in testimonials"
          :key="testimonial.id"
          class="comments"
        >
          <h4 class="our-comment">"{{ testimonial.comment }}"</h4>
          <p class="name">- {{ testimonial.name }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import testimonialData from '../../assets/data/app.json'

export default {
  data() {
    return {
      testimonials: testimonialData,
    }
  },
}
</script>

<style lang="scss" scoped>
.min-h-screen {
  min-height: 78vh;
}

.main-content {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 1rem;
  
  .content-item {
    h4 {
      font-size: 24px;
      
      &.our-comment {
        font-size: 16px;
      }
    }
    
    .content-img {
      border: 4px solid #fff;
      box-shadow: rgba(0, 0, 0, 0.5) 4px 4px 5px;
      width: 100%;
    }
    
    p {
      margin: 1rem;
      
      &.name {
        font-weight: 700;
      }
    }
    
    li {
      margin: 1rem;
      
      img {
        display: initial;
      }
    }

    .comments {
      background-color: #ccc;
      padding: 1ex;
      
      p {
        margin: 0;
      }
      
      &:nth-of-type(even) {
        background-color: #bfdae5;
      }
    }
  }
}

@media screen and (max-width: 375px) {
  .main-content {
    grid-template-columns: auto;
  }
}
</style>
