<template>
  <div class="main-wrapper">
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
      <a class="navbar-brand js-scroll-trigger" href="#about">
        <span class="d-block d-lg-none">Start Bootstrap</span>
        <span class="d-none d-lg-block">
          <img class="img-fluid img-profile rounded-circle mx-auto mb-2" src="./assets/profile.jpg" alt="">
        </span>
      </a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#about">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#experience">Experience</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#education">Education</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#skills">Skills</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#interests">Interests</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#awards">Awards</a>
          </li>
        </ul>
      </div>
    </nav>
    <div class="container-fluid p-0">
      <section class="resume-section p-3 p-lg-5 d-flex d-column" id="about">
        <div class="my-auto">
          <div class="subheading">Hi there! I'm</div>
          <h1 class="mb-0">{{ name }}
            <span class="text-primary">{{ surname }}</span>
          </h1>
          <div class="subheading mb-5">{{ address }}
            <a v-bind:href="'mailto:'+email+''">{{ email }}</a>
          </div>
          <p class="mb-5">{{ aboutMe }}</p>
          <ul class="list-inline list-social-icons mb-0">
            <li class="list-inline-item" v-for="soc in social" :key="soc.name">
              <a v-bind:href="''+ soc.url +''" target="_blank" rel="noreferrer">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i v-bind:class="'fa '+ soc.icon +' fa-stack-1x fa-inverse'"></i>
                </span>
              </a>
            </li>
          </ul>
        </div>
      </section>
      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="experience">
        <div class="my-auto">
          <h2 class="mb-5">Experience</h2>
          <div class="resume-item d-flex flex-column flex-md-row mb-5" v-for="job in experience" :key="job.position">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{ job.position }}</h3>
              <div class="subheading mb-3">{{ job.company }}</div>
              <p>{{ job.description }}</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">{{ job.startDate }} - {{ job.endDate }}</span>
            </div>
          </div>
        </div>
      </section>
      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="education">
        <div class="my-auto">
          <h2 class="mb-5">Education</h2>
          <div class="resume-item d-flex flex-column flex-md-row mb-5" v-for="edu in education" :key="edu.degree">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{ edu.name }}</h3>
              <div class="subheading mb-3">{{ edu.degree }}</div>
              <div>{{ edu.stream }}</div>
              <p>{{ edu.marks }}</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">{{ edu.startDate }} - {{ edu.endDate }}</span>
            </div>
          </div>
        </div>
      </section>
      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="skills">
        <div class="my-auto">
          <h2 class="mb-5">Skills</h2>
          <div class="subheading mb-3">Programming Languages &amp; Tools</div>
          <ul class="list-inline list-icons">
            <li class="list-inline-item" v-for="skill in skills" :key="skill.name">
              <i v-bind:class="'devicons '+ skill.icon +''" v-bind:title="''+ skill.level +''"></i>
            </li>
          </ul>
          <div class="subheading mb-3">Job Related Responsibility</div>
          <ul class="fa-ul mb-0">
            <li v-for="role in responsibility" :key="role.id">
              <i class="fa-li fa fa-check"></i>
              {{ role.text }}
            </li>
          </ul>
        </div>
      </section>
      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="interests">
        <div class="my-auto">
          <h2 class="mb-5">Interests</h2>
          <p class="mb-0"> {{ interest }}</p>
        </div>
      </section>
      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="awards">
        <div class="my-auto">
          <h2 class="mb-5">Awards &amp; Certifications</h2>
          <ul class="fa-ul mb-0">
            <li v-for="acc in accomplishment" :key="acc.id">
              <i class="fa-li fa fa-trophy text-warning"></i>
              {{ acc.text }} - {{ acc.company }} - {{ acc.date }}
            </li>
          </ul>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'My Portfolio',
      name: 'SATISH',
      surname: 'JHANWER',
      address: 'Ahmedabad, Gujarat 380013 · +91 (704) 339-4934 ·',
      email: 'satish.jhanwer@gmail.com',
      aboutMe:
        'Senior Full Stack Developer, Currently working on technology which includes Node.JS, React.JS, Golang, ExpressJS, jQuery, REST API etc.',
      social: [
        {
          name: 'facebook',
          url: 'https://www.facebook.com/satish.jhanwer89',
          icon: 'fa-facebook'
        },
        {
          name: 'twitter',
          url: 'https://twitter.com/satishjhanwer',
          icon: 'fa-twitter'
        },
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
          position: 'Senior Software Engineer',
          company: 'Sigma Infosolutions Ltd.',
          description:
            'Research and development of Golang, NodeJS, ReactJS. Designing and implementing software component assigned Write Unit Test case for the component built Do Code Review of the feature built by other team members Help team members technically whenever needed Process awareness for software development and implementing it Involvement in the recruitment process. Other Business activities as defined by Project Manager',
          startDate: 'Apr 2013',
          endDate: 'Present'
        },
        {
          position: 'Software Engineer',
          company: 'Sigma Infosolutions Ltd.',
          description:
            'Research and development of Groovy & Grails. Designing and implementing software component assigned Write Unit Test case for the component built Do Code Review of the feature built by other team members Help team members technically whenever needed Process awareness for software development and implementing it Involvement in the recruitment process. Other Business activities as defined by Project Manager',
          startDate: 'Apr 2012',
          endDate: 'Mar 2013'
        },
        {
          position: 'Associate Software Engineer',
          company: 'Sigma Infosolutions Ltd.',
          description:
            'Research and development of Groovy & Grails. Designing and implementing software component assigned Write Unit Test case for the component built Do Code Review of the feature built by other team members Help team members technically whenever needed Process awareness for software development and implementing it Involvement in the recruitment process. Other Business activities as defined by Project Manager',
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
          level: 'Upper Beignner'
        },
        {
          name: 'code',
          icon: 'devicons-code',
          level: 'Proficient'
        },
        {
          name: 'ubuntu',
          icon: 'devicons-ubuntu',
          level: 'Upper Beignner'
        },
        {
          name: 'bower',
          icon: 'devicons-bower',
          level: 'Upper Beignner'
        },
        {
          name: 'yeoman',
          icon: 'devicons-yeoman',
          level: 'Upper Beignner'
        },
        {
          name: 'grails',
          icon: 'devicons-grails',
          level: 'Upper Beignner'
        },
        {
          name: 'groovy',
          icon: 'devicons-groovy',
          level: 'Upper Beignner'
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
          level: 'Upper Beignner'
        },
        {
          name: 'go',
          icon: 'devicons-go',
          level: 'Beignner'
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
          text: 'Unit Testing'
        }
      ],
      interest:
        'Apart from being a web developer, I enjoy spending time with my family and friends. I enjoy playing games on PS4, I follow a number of sci-fi and fantasy genre movies and television shows, and I spend a large amount of my free time exploring the latest technolgy advancements in the front-end web development world.',
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

<style>
</style>
