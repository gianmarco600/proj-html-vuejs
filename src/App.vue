<template>
  <div id="app">
    <Header :logo="logo" :links="linksLabel"/>
    <Jumbo 
    :jumboDatas="mainContents.jumbo" 
    />
    <Main 
    :mainDatas="mainContents"
    />
    <Footer
    :footerDatas="footer"
    />
    <!-- <FixedMenu/> -->
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import Jumbo from './components/Jumbo.vue'
// import FixedMenu from './components/FixedMenu.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Jumbo,
    // FixedMenu
  },
  data(){
    return{
      logo:'light-logo.png',
      linksLabel:[
        'home',
        'pages',
        'courses',
        'features',
        'blog',
        'shop'
      ],
      mainContents:{
        jumbo:{
          texts:{
            main:'learn at your own pace!',
            sub:'get teamed up whith people of the same will',
            src:[
              'home-6-hero-left-person.png',
              'home-6-hero-right-person-195x300.png',
              'home-6-hero-poster-final.jpg'
            ]
          }
        },
        intro:{
          main:"Let passion and determination be the guide along the way and develop at your own pace that's comfortable.",
          cardsDatas:{
            card1:{
              num: '1999',
              sub: 'finished sessions'
            },
            card2:{
              num:'3.092+',
              sub: 'enrolled learners'
            },
            card3:{
              num:'200',
              sub: 'online instructors'
            },
            card4:{
              num:' 100 % ',
              sub: 'Satisfaction rate'
            }
          },
          column1CardDatas:{
            card1:{
              label:'Graphic Design',
              text:'Have a passion for graphics and arts? Show your talents with confidence and self-assertiveness.',
              src:'home-6-service-image-01.png'
            },
            card2:{
              label:'Idea Discussion',
              text:'Get teamed up with the specialists who work and teach coding for years at famous universities.',
              src:'home-6-service-image-03.png'
            }
          },
          column2CardDatas:{
            card1:{
              label:'Business Administration	',
              text:'Learners are encouraged to study the mechanism and structure of system administration.',
              src:'home-6-service-image-02.png'
            },
            card2:{
              label:'Web Development',
              text:'Learn to start building a webpage from scratch. You decide your own pace, course and speed.',
              src:'home-6-service-image-04.png'
            }
          },
          rightBanner:{
            intro:'Together We Can Create',
            main:"Services We Can Provide For My Clients.",
            list:[
              'Select & customize courses to your preferences',
              'Change the tutor and make arrangements',
              'Participate in events to join others',
              'Get the desired certificate delivered at house'
            ]
          }
        },
        courses:{
          intro:'Choose a course to get started',
          main:'Latest Featured Courses',
          coursesList:[
            {
              price:'free',
              descr:'Personal Finance: Financial Security Thinking & Principles',
              lessons: 2,
              students: 96,
              src: 'course-02-480x298.jpg'
            },
            {
              price:'free',
              descr:'Customer-centric Info-Tech Strategies',
              lessons: 24,
              students: 823,
              src: 'course-featured-image-01-480x298.jpg'
            },
            {
              price:'$26.00',
              descr:'Academic Listening and Note-taking',
              lessons: 14,
              students: 68,
              src:'stock-full-hd-03-480x298.jpg'
            },
            {
              price:'$40.00',
              descr:'Learning to Write as a Professional Author',
              lessons: 20,
              students: 51,
              src:'stock-full-hd-04-480x298.jpg'
            },
            {
              price:'$19.00',
              descr:'Open Programming Courses for Everyone: Python',
              lessons: 17,
              students: 63,
              src:'stock-full-hd-05-480x298.jpg'
            },
            {
              price:'$39.00',
              descr:'Master jQuery in a Short Period of Time',
              lessons: 6,
              students: 52,
              src:'stock-full-hd-06-480x298.jpg'
            }
            
          ]
        },
        feed:{
          main:'Why People Talk About MaxCoach?',
          text:'I am free to learn at my own pace, follow my own schedule and choose the subject I like. Great study portal for people like me.',
          clients:[
                  'client-logo-colored-01.png',
                  'client-logo-colored-02.png',
                  'client-logo-colored-03.png',
                  'client-logo-colored-04.png',
                  'client-logo-colored-05.png',
                  'client-logo-colored-06.png'
                ]
        },
        blog:{
          intro:'Enjoy reading on maxCoach',
          main:'Latest on Our Blogs',
          cards:[
            {
              tema:'business',
              main:'Ten Benefits Of Rentals That May Change Your Perspective',
              data:' dec 29, 2020',
              views:'1241',
              src:'artist-blog-01-480x325.jpg'
            },
            {
              tema:'business',
              main:'10 Things Successful Mompreneurs Do Different',
              data:' dec 29, 2020',
              views:'1811',
              src:'artist-blog-02-480x325.jpg'
            },
            {
              tema:'business',
              main:'How Stay Calm from the First Time.',
              data:' dec 29, 2020',
              views:'1361',
              src:'artist-blog-03-480x325.jpeg'
            }
          ]
        },
        prefoot:{
          intro:'Wanna transform your life?',
          main:'Glad to Help You Learn',
          cols:[
            {
              main:'Idea Discussion',
              text:'Get teamed up with the specialists who work and teach coding for years at famous universities.'
            },
            {
              main:'Web Development',
              text:'Learn to start building a webpage from scratch. You decide your own pace, course and speed.'
            },
            {
              main:'System Administration',
              text:'Learners are encouraged to study the mechanism and structure of system administration. '
            },
            {
              main:'Graphic Design',
              text:'Have a passion for graphics and arts? Show your talents with confidence and self-assertiveness. '
            }
          ],
          cta:{
            intro:'Start today for getting Online Certification',
            main:'You can be your own guiding star with our help!'
          }
        },
        
      },
      footer:{
          address:[
            '382 NE 191st St # 87394 Miami, FL 33179-3899',
            '+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)',
            'support@maxcoach.com'
          ],
          explore1:[
            'Start here',
            'Blog',
            'About us'
          ],
          explore2:[
            'Success story',
            'Courses',
            'Contact us'
          ],
          information:[
            'Membership',
            'Purchase guide',
            'Privacy policy',
            'Terms of services'
          ]
        }
      }
    }
  }

</script>

<style lang="scss">
@import '@/style/commons.scss';

#app {
  font-family: 'Quicksand' sans-serif;
  
}
</style>
