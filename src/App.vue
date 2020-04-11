<template>
  <div class="main-wrapper">
    <Navbar landing-link="#about" :navItems="navItems" id="sideNav"></Navbar>
    <div class="container-fluid p-0">
      <AboutMe :user="user" :social="social" id="about"></AboutMe>
      <Experience :experience="experience" id="experience"></Experience>
      <Education :education="education" id="education"></Education>
      <Skills
        :skills="skills"
        :responsibility="responsibility"
        id="skills"
      ></Skills>
      <Interests :interest="interest" id="interests"></Interests>
      <Awards :accomplishment="accomplishment" id="awards"></Awards>
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Skills from './components/Skills.vue'
import Awards from './components/Awards.vue'
import AboutMe from './components/AboutMe.vue'
import Education from './components/Education.vue'
import Interests from './components/Interests.vue'
import Experience from './components/Experience.vue'

export default {
  components: {
    Navbar,
    Skills,
    Awards,
    AboutMe,
    Education,
    Interests,
    Experience
  },
  data () {
    return {
      title: 'My Portfolio',
      navItems: [
        { title: 'About', link: '#about' },
        { title: 'Experience', link: '#experience' },
        { title: 'Education', link: '#education' },
        { title: 'Skills', link: '#skills' },
        { title: 'Interests', link: '#interests' },
        { title: 'Awards', link: '#awards' }
      ],
      user: {
        name: 'SATISH',
        surname: 'JHANWER',
        address: 'Pune, Maharashtra 411057 · +91 (704) 339-4934 ·',
        email: 'satish.jhanwer@gmail.com',
        introduction:
          'Sr. UI Developer, Currently working on technology which includes Node.JS, React.JS, Golang, ExpressJS, MongoDB, Docker, Kubernetes, Microservices, REST API etc.'
      },
      social: [
        {
          name: 'linkedin',
          url: 'https://www.linkedin.com/in/satishjhanwer/',
          icon: 'fa-linkedin'
        },
        {
          name: 'github',
          url: 'https://github.com/satishjhanwer',
          icon: 'fa-github'
        }
      ],
      experience: [
        {
          position: 'Senior UI Developer',
          company: 'Barclays',
          description:
            'Working on technology which includes Node.JS, React.JS, Typescript, ExpressJS, Microservices, REST API etc',
          startDate: 'Dec 2018',
          endDate: 'Till Now'
        },
        {
          position: 'Associate Technical Architect',
          company: 'Sigma Infosolutions Ltd.',
          description:
            'Research and development of Golang, NodeJS, ReactJS. Designing and implementing software component assigned Write Unit Test case for the component built Do Code Review of the feature built by other team members Help team members technically whenever needed Process awareness for software development and implementing it Involvement in the recruitment process. Providing End to End solutions for the complex problem.',
          startDate: 'Sep 2018',
          endDate: 'Dec 2018'
        },
        {
          position: 'Senior Software Engineer',
          company: 'Sigma Infosolutions Ltd.',
          description:
            'Research and development of Golang, NodeJS, ReactJS. Designing and implementing software component assigned Write Unit Test case for the component built Do Code Review of the feature built by other team members Help team members technically whenever needed Process awareness for software development and implementing it Involvement in the recruitment process. Other Business activities as defined by Project Manager.',
          startDate: 'Apr 2013',
          endDate: 'Aug 2018'
        },
        {
          position: 'Software Engineer',
          company: 'Sigma Infosolutions Ltd.',
          description:
            'Research and development of Groovy & Grails. Designing and implementing software component assigned Write Unit Test case for the component built Do Code Review of the feature built by other team members Help team members technically whenever needed Process awareness for software development and implementing it Involvement in the recruitment process. Other Business activities as defined by Project Manager.',
          startDate: 'Apr 2012',
          endDate: 'Mar 2013'
        },
        {
          position: 'Associate Software Engineer',
          company: 'Sigma Infosolutions Ltd.',
          description:
            'Research and development of Groovy & Grails. Designing and implementing software component assigned Write Unit Test case for the component built Do Code Review of the feature built by other team members Help team members technically whenever needed Process awareness for software development and implementing it Involvement in the recruitment process. Other Business activities as defined by Project Manager.',
          startDate: 'Oct 2010',
          endDate: 'Mar 2012'
        }
      ],
      education: [
        {
          name: 'Rajasthan Technical University',
          degree: 'Bachelor of Technology',
          stream: 'Information Technology',
          marks: '75%',
          startDate: 'Jul 2006',
          endDate: 'Jul 2010'
        },
        {
          name: 'Board of Secondary Education, Rajasthan',
          degree: 'Senior Secondary (12th)',
          stream: 'Science Maths',
          marks: '78%',
          startDate: 'Jul 2005',
          endDate: 'May 2006'
        },
        {
          name: 'Board of Secondary Education, Rajasthan',
          degree: 'Secondary (10th)',
          stream: '',
          marks: '72%',
          startDate: 'Jul 2003',
          endDate: 'May 2004'
        }
      ],
      skills: [
        {
          name: 'javascript',
          icon: 'devicons-javascript',
          level: 'Proficient'
        },
        {
          name: 'react',
          icon: 'devicons-react',
          level: 'Proficient'
        },
        {
          name: 'nodejs',
          icon: 'devicons-nodejs',
          level: 'Proficient'
        },
        {
          name: 'html',
          icon: 'devicons-html5',
          level: 'Proficient'
        },
        {
          name: 'css3',
          icon: 'devicons-css3',
          level: 'Proficient'
        },
        {
          name: 'docker',
          icon: 'devicons-docker',
          level: 'Proficient'
        },
        {
          name: 'mongodb',
          icon: 'devicons-mongodb',
          level: 'Upper Beginner'
        },
        {
          name: 'code',
          icon: 'devicons-code',
          level: 'Proficient'
        },
        {
          name: 'ubuntu',
          icon: 'devicons-ubuntu',
          level: 'Upper Beginner'
        },
        {
          name: 'bower',
          icon: 'devicons-bower',
          level: 'Upper Beginner'
        },
        {
          name: 'yeoman',
          icon: 'devicons-yeoman',
          level: 'Upper Beginner'
        },
        {
          name: 'grails',
          icon: 'devicons-grails',
          level: 'Upper Beginner'
        },
        {
          name: 'groovy',
          icon: 'devicons-groovy',
          level: 'Upper Beginner'
        },
        {
          name: 'git',
          icon: 'devicons-git',
          level: 'Proficient'
        },
        {
          name: 'bitbucket',
          icon: 'devicons-bitbucket',
          level: 'Proficient'
        },
        {
          name: 'jira',
          icon: 'devicons-jira',
          level: 'Upper Beginner'
        },
        {
          name: 'go',
          icon: 'devicons-go',
          level: 'Beginner'
        },
        {
          name: 'jquery',
          icon: 'devicons-jquery',
          level: 'Proficient'
        },
        {
          name: 'grunt',
          icon: 'devicons-grunt',
          level: 'Proficient'
        },
        {
          name: 'gulp',
          icon: 'devicons-gulp',
          level: 'Proficient'
        },
        {
          name: 'npm',
          icon: 'devicons-npm',
          level: 'Proficient'
        }
      ],
      responsibility: [
        {
          id: 1,
          text: 'Cross Browser Testing & Debugging'
        },
        {
          id: 2,
          text: 'Involvement in Recruitment Process'
        },
        {
          id: 3,
          text: 'Agile Development & Scrum'
        },
        {
          id: 4,
          text: 'Help Team Members whenever needed'
        },
        {
          id: 5,
          text: 'Unit & Functional Testing'
        }
      ],
      interest:
        'Apart from being a web developer, I enjoy spending time with my family and friends. I enjoy playing games on PS4, I love watching sci-fi, fantasy, comedy movies and web series, and I spend a large amount of my free time exploring the latest technolgy advancements in the front-end web development world.',
      accomplishment: [
        {
          id: 1,
          text: 'Quarterly Appreciation Award',
          date: 'Aug 2015',
          company: 'Sigma Infosolutions Ltd'
        },
        {
          id: 2,
          text: 'Spot Award',
          date: 'Oct 2014',
          company: 'Sigma Infosolutions Ltd'
        },
        {
          id: 3,
          text: 'Debut Employee',
          date: 'Nov 2010',
          company: 'Sigma Infosolutions Ltd'
        }
      ]
    }
  },
  mounted () {
    const $ = this.jquery
    this.$nextTick(() => {
      // our custom jQuery code goes here
      $('a.js-scroll-trigger[href*="#"]:not([href="#"])').click(function () {
        if (
          location.pathname.replace(/^\//, '') ===
            this.pathname.replace(/^\//, '') &&
          location.hostname === this.hostname
        ) {
          var target = $(this.hash)
          target = target.length
            ? target
            : $('[name=' + this.hash.slice(1) + ']')
          if (target.length) {
            $('html, body').animate(
              {
                scrollTop: target.offset().top
              },
              1000,
              'easeInOutExpo'
            )
            return false
          }
        }
      })

      // Closes responsive menu when a scroll trigger link is clicked
      $('.js-scroll-trigger').click(function () {
        $('.navbar-collapse').collapse('hide')
      })

      // Activate scrollspy to add active class to navbar items on scroll
      $('body').scrollspy({
        target: '#sideNav'
      })
    })
  }
}
</script>

<style></style>
