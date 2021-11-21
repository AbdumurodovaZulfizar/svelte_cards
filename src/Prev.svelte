<script>
	window.addEventListener("DOMContentLoaded", () => {
    const slides = document.querySelectorAll(".my_card"),
        wrapper = document.querySelector(".slide_wrapper"),
        inner_wrapper = document.querySelector(".wrapper"),
        width = getComputedStyle(wrapper).width;
  let offset = 0;

  const handleClick = () => {
    if (offset == 0) {
      offset = (+width.slice(0, width.length - 2) * (slides.length - 1))/3.5;
    } else {
      offset -= +width.slice(0, width.length - 2)/3.5;
    }
    inner_wrapper.style.transform = `translateX(-${offset}px)`
  }
  })
</script>

<button on:click={handleClick} class="self-center text-5xl px-3" id="prev" role="button">
  <i class="fas fa-chevron-left"></i>
</button>