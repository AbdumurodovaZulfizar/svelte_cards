<script>
  window.addEventListener("DOMContentLoaded", () => {
  const slides = document.querySelectorAll(".my_card"),
        wrapper = document.querySelector(".slide_wrapper"),
        inner_wrapper = document.querySelector(".wrapper"),
        width = getComputedStyle(wrapper).width,
        prev = document.querySelector("#prev"),
        next = document.querySelector("#next");
  let offset = 0;

  next.addEventListener("click", () => {
    if (offset == (+width.slice(0, width.length - 2) * (slides.length - 1))/3) {
      offset = 0;
    } else {
      offset += +width.slice(0, width.length - 2)/3;
    }
    inner_wrapper.style.transform = `translateX(-${offset}px)`
  })

  prev.addEventListener("click", () => {
    if (offset == 0) {
      offset = (+width.slice(0, width.length - 2) * (slides.length - 1))/3;
    } else {
      offset -= +width.slice(0, width.length - 2)/3;
    }
    inner_wrapper.style.transform = `translateX(-${offset}px)`
  })
})
</script>

<div class="self-center text-5xl px-3" id="next" role="button">
  <i class="fas fa-chevron-right"></i>
</div>