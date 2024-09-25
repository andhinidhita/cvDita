<template>
  <div class="cv">
    <header>
      <img :src="profileImage" alt="Profile Picture" class="profile-image" />
      <div class="header-text">
        <h1>{{ name }}</h1>
        <p>{{ jobTitle }}</p>
        <p>{{ contactInfo }}</p>
      </div>
    </header>

    <section>
      <h2>About Me</h2>
      <p>{{ bio }}</p>
    </section>

    <section>
      <h2>Education</h2>
      <ul>
        <li v-for="edu in pendidikan" :key="edu.institution">
          <h3>{{ edu.degree }}</h3>
          <p>{{ edu.institution }} - {{ edu.dates }}</p>
        </li>
      </ul>
    </section>

    <section>
      <h2>Work Experience</h2>
      <ul>
        <li v-for="job in pengalaman" :key="job.company">
          <h3>{{ job.position }}</h3>
          <p>{{ job.company }} - {{ job.dates }}</p>
          <p>{{ job.description }}</p>
        </li>
      </ul>
    </section>

    <section>
      <h2>Organizational Experience</h2>
      <ul>
        <li v-for="org in pengalamanOrganisasi" :key="org.organization">
          <h3>{{ org.position }}</h3>
          <p>{{ org.organization }} - {{ org.dates }}</p>
          <p>{{ org.description }}</p>
        </li>
      </ul>
    </section>

    <section>
      <h2>Skills</h2>
      <ul>
        <li v-for="skill in keterampilan" :key="skill">{{ skill }}</li>
      </ul>
    </section>

    <section>
      <h2>Committee</h2>
      <ul>
        <li v-for="committee in committees" :key="committee.event">
          <h3>{{ committee.role }}</h3>
          <p>{{ committee.event }} - {{ committee.year }}</p>
          <p>{{ committee.description }}</p>
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup>
const name = 'Andhini Ditha Audia';
const jobTitle = 'UI/UX Designer';
const contactInfo = 'Email: ditaaudy43@gmail.com | Phone: +62 822 2819 4574';
const profileImage = 'dita.jpg'; // Ganti dengan jalur gambar yang sesuai

// Adding a brief bio
const bio = "I am an active student at Brawijaya University, vocational faculty of information technology. With a strong background in the field of multimedia and technology, I am excited to continue developing and learning in the world of UI/UX design.";

const pendidikan = [
  {
    degree: 'Multimedia',
    institution: 'Matesih State High School',
    dates: '2020 - 2023'
  },
  {
    degree: 'Associate in Information Technology',
    institution: 'Brawijaya University',
    dates: '2023 - Present'
  }
];

const pengalaman = [
  {
    position: 'printing',
    company: 'CV Mutiara',
    dates: 'des 2021 - feb 2022',
    description: 'skills in operating software such as Adobe Illustrator, Photoshop, and other print preparation programs..'
  },
  {
    position: 'digital printing design',
    company: 'Indomedia Printing',
    dates: 'aug 2022 - okt 2022',
    description: 'skills in operating software such as Adobe Illustrator, Photoshop, and other print preparation programs..'
  }
];

const pengalamanOrganisasi = [
  {
    position: 'HMPSTI Intern Staff',
    organization: 'Information Technology Study Program Student Association, Puskominfo Division',
    dates: 'Sept 2023 - Dec 2023',
    description: 'Handle and design HMPSTI social media accounts.'
  }
];

const keterampilan = [
  'Corel Draw', 
  'Photoshop', 
  'Adobe Animate', 
  'Figma', 
  'Canva' 
];

const committees = [
  {
    role: 'consume',
    event: 'Creanomic',
    year: '2024',
    description: 'contacting caterers for events and being responsible for the sponsorship division during events.'
  }
  
];
</script>

<style>
.cv {
  max-width: 800px;
  margin: auto;
  padding: 20px;
  background-color: #FFF4EA;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

header {
  display: flex;
  align-items: center;
  margin-bottom: 30px;
}

.profile-image {
  width: 100px; /* Sesuaikan ukuran gambar */
  height: 125px; /* Sesuaikan ukuran gambar */
  border-radius: 0%; /* Membuat gambar bulat */
  margin-right: 20px; /* Spasi antara gambar dan teks */
}

.header-text {
  text-align: left;
}

h1 {
  font-size: 2.5em;
  margin: 0;
}

h2 {
  border-bottom: 2px solid #ccc;
  padding-bottom: 5px;
  margin-top: 20px;
  color: #333;
}

section {
  margin-bottom: 20px;
}

ul {
  list-style-type: none; /* Menghilangkan bullet points */
  padding: 0; /* Menghilangkan padding */
}

li {
  margin-bottom: 10px;
  padding: 10px;
  background-color: #fff; /* Warna latar belakang item daftar */
  border: 1px solid #ddd; /* Garis batas item daftar */
  border-radius: 5px; /* Sudut melingkar */
}

li h3 {
  margin: 0;
  color: #800000; /* Warna teks judul pekerjaan */
}

p {
  margin: 5px 0; /* Margin atas dan bawah */
  color: #555; /* Warna teks deskripsi */
}
</style>
