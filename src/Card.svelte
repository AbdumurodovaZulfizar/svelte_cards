<script>
	window.addEventListener("DOMContentLoaded", () => {
    const slides = document.querySelectorAll(".my_card"),
        wrapper = document.querySelector(".slide_wrapper"),
        inner_wrapper = document.querySelector(".wrapper"),
        width = getComputedStyle(wrapper).width;
        inner_wrapper.style.width = 100*(slides.length)/3.5 + '%';
        inner_wrapper.style.transition = '0.5s ease';
    slides.forEach(slide => {
    slide.style.width = width/3.5;
    })
  })
</script>

<div class="shadow-md rounded-md mx-3 my-2 my_card transition ease-out duration-700 transform hover:scale-105">
  <div class="flex justify-between bg-gray-100 rounded-t-md">
    <div class="flex">
      <img src="./restaurant.jpg" alt="image" class="w-24 p-3" />
      <div class="py-3 flex flex-col justify-between">
        <p class="text-xl text-gray-800 font-semibold">Project name</p>
        <p class="text-base text-gray-600 font-semibold"><i class="fas fa-check-square text-black"></i><span class="px-3">Company name</span></p>
      </div>
    </div>
    <div class="flex flex-col justify-between p-3 place-items-end">
      <i class="far fa-bookmark"></i>
      <p>5 hours ago</p>
    </div>
  </div>
  <div>
    <div class="p-3">
      <p class="leading-8"><i class="fas fa-clock"></i><span class="px-2 text-gray-600">10hr/per week</span></p>
      <p class="leading-8"><i class="fas fa-medal"></i><span class="px-2 text-gray-600">Certificate/Recommendation Letter</span></p>
      <p class="leading-8"><i class="fas fa-map-marker-alt"></i><span class="px-2 text-gray-600">Remote</span></p>
      <div class="flex flex-wrap pt-3">
        <div class="px-2 bg-gray-200 mr-3 my-1 rounded-md">Front-end Engineer</div>
        <div class="px-2 bg-gray-200 mr-3 my-1 rounded-md">Backend Engineer</div>
        <div class="px-2 bg-gray-200 mr-3 my-1 rounded-md">UX/UI Designer</div>
        <div class="px-2 bg-gray-200 my-1 rounded-md">QA Tester</div>
      </div>
    </div>
  </div>
</div>
