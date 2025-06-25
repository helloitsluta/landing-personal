<template>
  <section class="bg-dark text-white py-5" id="projects">
    <div class="container">
      <h2 class="text-center fw-bold mb-5">Selected Projects</h2>
      <div class="row g-4">
        <div class="col-md-4" v-for="project in projects" :key="project.title">
          <div class="card h-100 bg-secondary text-white border-0 shadow">
            <img :src="project.image" class="card-img-top" :alt="project.title" />
            <div class="card-body">
              <h5 class="card-title fw-bold">{{ project.title }}</h5>
              <p class="card-text">{{ project.description }}</p>
              <a :href="project.link" class="btn btn-outline-light btn-sm" target="_blank">View Project</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: '판매자 플랫폼',
    description: 'React + Tailwind 기반의 반응형 앱으로, 판매자 대상의 주문 처리 기능을 개발.',
    image: 'https://via.placeholder.com/600x400?text=Project+1',
    link: '#',
  },
  {
    title: '송장 자동화 웹앱',
    description: '엑셀 파일 양식을 이용해 송장을 자동 처리하는 시스템 개발.',
    image: 'https://via.placeholder.com/600x400?text=Project+2',
    link: '#',
  },
  {
    title: '업무지표 대시보드',
    description: 'SQL 쿼리와 Redash를 연동하여 실시간 통계 대시보드를 구성.',
    image: 'https://via.placeholder.com/600x400?text=Project+3',
    link: '#',
  },
]
</script>