<template>
<section class="review">
        <div class="container">
        <div class="swiper testimonial-wrapper js-slider container">

       <div class="swiper-wrapper">

            <!-- Slide 1 -->
            <div class="swiper-slide  testimonial-card">
              <div class="testimonial-content">
                <div class="test">
                <div class="starts">
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star"></i>
                </div>
                <div class="quotes">
                  <p class="quote">
                    Incredible attention to detail and professionalism. Our
                    website turned out better than we imagined!
                  </p>
                </div>
                <div class="author-desig">
                  <p class="author">— Hana Saito</p>
                  <p class="designation">Marketing Director, BrightWave</p>
                </div>
                </div>
               
              </div>
              <div class="testimonial-image">
                <img src="assets/Image.svg" alt="Hana Saito" />
              </div>
            </div>
        
           
           <div class="swiper-slide testimonial-card">
              <div class="testimonial-content">
                <div class="test">
                <div class="starts">
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star-o"></i>
                </div>
                <div class="quotes">
                  <p class="quote">
                    Reliable, efficient, and creative. The 
                    best experience we've had with a development team.
                  </p>
                </div>
                <div class="author-desig">
                  <p class="author">— Daniel Foster</p>
                  <p class="designation">Founder, ElevateApps</p>
                </div>
              </div>
              </div>
              <div class="testimonial-image">
                <img src="assets/Image_(1).svg" alt="Daniel Foster" />
              </div>
            </div>
      
            <div class="swiper-slide testimonial-card">
              <div class="testimonial-content">
                <div class="test">
                <div class="starts">
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star"></i>
                  <i class="fa fa-star"></i>
                </div>
                <div class="quotes">
                  <p class="quote">
                    Seamless process and outstanding results! 
                    The team exceeded expectations at every step.
                  </p>
                </div>
                <div class="author-desig">
                  <p class="author">— Aoife Gallagher</p>
                  <p class="designation">CTO, NexaTech</p>
                </div>
                </div>
              </div>
              <div class="testimonial-image">
                <img src="assets/Image_(2).svg" alt="Aoife Gallagher" />
              </div>
             
            </div>
      
        
          <!-- Optional: Swiper pagination if needed -->
          
        </div>
        <div class="swiper-pagination swiper-pag"></div>
        </div>
      </div>
      </section>

</template>


<script>
import {onMounted} from 'vue'
import Swiper from 'swiper'
import 'swiper/swiper-bundle.css'
onMounted(()=>{
      const swiper = new Swiper('.swiper', {
    slidesPerView:1,
    spaceBetween:60,
    autoplay: {
      delay: 3000,
      disableOnInteraction: false,
      pauseOnMouseEnter: true,
    },
    pagination: {
      el: '.swiper-pagination',
      clickable: true,
    },
  });

})
</script>

