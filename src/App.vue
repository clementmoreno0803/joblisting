<template>
  <div class="container">
    <table v-for="(job, index) in jobs" :key="index">
      <tr>
        {{
          job.logo
        }}
      </tr>
      <div class="infos">
        <div class="company">
          <tr>
            {{
              job.company
            }}
          </tr>
          <div v-if="job.new" id="new">
            <tr>
              New
            </tr>
          </div>
          <div v-if="job.featured" id="featured">
            <tr>
              Featured
            </tr>
          </div>
          <tr>
            {{
              job.position
            }}
          </tr>
          <div class="position_info">
            <tr>
              {{
                job.postedAt
              }}
            </tr>
            <tr>
              {{
                job.contract
              }}
            </tr>
            <tr>
              {{
                job.location
              }}
            </tr>
          </div>
          <tr id="language">
            {{
              job.languages.join("")
            }}
          </tr>
        </div>
      </div>
    </table>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      jobs: [
        {
          id: 1,
          company: "Photosnap",
          logo: "./images/photosnap.svg",
          new: true,
          featured: true,
          position: "Senior Frontend Developer",
          role: "Frontend",
          level: "Senior",
          postedAt: "1d ago",
          contract: "Full Time",
          location: "USA Only",
          languages: ["HTML", "CSS", "JavaScript"],
          tools: [],
        },
        {
          id: 2,
          company: "Manage",
          logo: "./images/manage.svg",
          new: true,
          featured: true,
          position: "Fullstack Developer",
          role: "Fullstack",
          level: "Midweight",
          postedAt: "1d ago",
          contract: "Part Time",
          location: "Remote",
          languages: ["Python"],
          tools: ["React"],
        },
        {
          id: 3,
          company: "Account",
          logo: "./images/account.svg",
          new: true,
          featured: false,
          position: "Junior Frontend Developer",
          role: "Frontend",
          level: "Junior",
          postedAt: "2d ago",
          contract: "Part Time",
          location: "USA Only",
          languages: ["JavaScript"],
          tools: ["React", "Sass"],
        },
        {
          id: 4,
          company: "MyHome",
          logo: "./images/myhome.svg",
          new: false,
          featured: false,
          position: "Junior Frontend Developer",
          role: "Frontend",
          level: "Junior",
          postedAt: "5d ago",
          contract: "Contract",
          location: "USA Only",
          languages: ["CSS", "JavaScript"],
          tools: [],
        },
        {
          id: 5,
          company: "Loop Studios",
          logo: "./images/loop-studios.svg",
          new: false,
          featured: false,
          position: "Software Engineer",
          role: "Fullstack",
          level: "Midweight",
          postedAt: "1w ago",
          contract: "Full Time",
          location: "Worldwide",
          languages: ["JavaScript"],
          tools: ["Ruby", "Sass"],
        },
        {
          id: 6,
          company: "FaceIt",
          logo: "./images/faceit.svg",
          new: false,
          featured: false,
          position: "Junior Backend Developer",
          role: "Backend",
          level: "Junior",
          postedAt: "2w ago",
          contract: "Full Time",
          location: "UK Only",
          languages: ["Ruby"],
          tools: ["RoR"],
        },
        {
          id: 7,
          company: "Shortly",
          logo: "./images/shortly.svg",
          new: false,
          featured: false,
          position: "Junior Developer",
          role: "Frontend",
          level: "Junior",
          postedAt: "2w ago",
          contract: "Full Time",
          location: "Worldwide",
          languages: ["HTML", "JavaScript"],
          tools: ["Sass"],
        },
        {
          id: 8,
          company: "Insure",
          logo: "./images/insure.svg",
          new: false,
          featured: false,
          position: "Junior Frontend Developer",
          role: "Frontend",
          level: "Junior",
          postedAt: "2w ago",
          contract: "Full Time",
          location: "USA Only",
          languages: ["JavaScript"],
          tools: ["Vue", "Sass"],
        },
        {
          id: 9,
          company: "Eyecam Co.",
          logo: "./images/eyecam-co.svg",
          new: false,
          featured: false,
          position: "Full Stack Engineer",
          role: "Fullstack",
          level: "Midweight",
          postedAt: "3w ago",
          contract: "Full Time",
          location: "Worldwide",
          languages: ["JavaScript", "Python"],
          tools: ["Django"],
        },
        {
          id: 10,
          company: "The Air Filter Company",
          logo: "./images/the-air-filter-company.svg",
          new: false,
          featured: false,
          position: "Front-end Dev",
          role: "Frontend",
          level: "Junior",
          postedAt: "1mo ago",
          contract: "Part Time",
          location: "Worldwide",
          languages: ["JavaScript"],
          tools: ["React", "Sass"],
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#new {
  width: fit-content;
  padding: 5px 15px;
  background: rgb(111, 143, 111);
  color: white;
  border-radius: 25px;
  font-size: 0.75em;
}
#featured {
  width: fit-content;
  padding: 5px 15px;
  background: rgb(38, 39, 38);
  color: white;
  border-radius: 25px;
  font-size: 0.75em;
}
#languages {
  padding: 5px;
  background: red;
}
</style>
