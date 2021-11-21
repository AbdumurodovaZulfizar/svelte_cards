<script>
	window.addEventListener("DOMContentLoaded", () => {
    const slides = document.querySelectorAll(".my_card"),
        wrapper = document.querySelector(".slide_wrapper"),
        inner_wrapper = document.querySelector(".wrapper"),
        width = getComputedStyle(wrapper).width;
        inner_wrapper.style.width = 100*(slides.length)/3 + '%';
        inner_wrapper.style.transition = '0.5s ease';
    slides.forEach(slide => {
    slide.style.width = width/3;
    })
  })
  const src = "https://blog.hubspot.com/hs-fs/hubfs/landing-page-template-architecture.jpg?width=450&name=landing-page-template-architecture.jpg";
  const project = {
    name: "Project name",
    company: "Company name",
    time: "5 hours ago",
    duration: "10hr/per week",
    cert: "Certificate/Recommendation Letter",
    type: "Remote",
    tools: ["Front-end Engineer", "Backend Engineer", "UX/UI Designer", "QA Tester"]
  }
</script>

<div class="shadow-md rounded-md mx-3 my-2 my_card transition ease-out duration-700 transform hover:scale-105">
  <div class="flex justify-between bg-gray-100 rounded-t-md">
    <div class="flex">
      <img class="w-24 p-3" src={src} alt="" /> 
      <div class="py-3 flex flex-col justify-between">
        <p class="text-xl text-gray-800 font-semibold">{project.name}</p>
        <p class="text-base text-gray-600 font-semibold"><i class="fas fa-check-square text-black"></i><span class="px-3">{project.company}</span></p>
      </div>
    </div>
    <div class="flex flex-col justify-between p-3 place-items-end">
      <i class="far fa-bookmark"></i>
      <p>{project.time}</p>
    </div>
  </div>
  <div>
    <div class="p-3">
      <p class="leading-8"><i class="fas fa-clock"></i><span class="px-2 text-gray-600">{project.duration}</span></p>
      <p class="leading-8"><i class="fas fa-medal"></i><span class="px-2 text-gray-600">{project.cert}</span></p>
      <p class="leading-8"><i class="fas fa-map-marker-alt"></i><span class="px-2 text-gray-600">{project.type}</span></p>
      <div class="flex flex-wrap pt-3">
        {#each project.tools as tool}
        <div class="px-2 bg-gray-200 mr-3 my-1 rounded-md">{tool}</div>
        {/each}
      </div>
    </div>
  </div>
</div>
