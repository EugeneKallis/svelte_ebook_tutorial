<script>
  import bookCover from "$assets/book_cover.png";
  import phoneCover from "$assets/phone_cover.png";
  import { Button } from "$components";
  let { children } = $props();
</script>

<section class="hero">
  <div class="hero-showcase text-center bold">
    <h1 class="purple">Move to</h1>
    <h1 class="purple mb-xs">Spain</h1>
    <h4 class="italic semi-bold">Theres no need fldsdfsdkflsdf</h4>
    <img class="book-cover" src={bookCover} alt="" />
    <img src={phoneCover} alt="" class="phone-cover" />
  </div>
  <div class="hero-text white text-center">
    {#if children}
      {@render children()}
    {:else}
      <h3>This ebook will</h3>
      <h3>save you money</h3>
      <h3 class="mb-m">Time and nerves</h3>
      <p class="light-grey mb-l">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed auctor, arcu a efficitur ullamcorper, dui velit ullamcorper velit, vel iaculis neque velit
        vel nunc. Sed vel ligula vel arcu tincidunt scelerisque.
      </p>
      <Button>Purchase Ebook for 10$</Button>
    {/if}
  </div>
</section>

<style>
  .hero {
    display: flex;
    height: 100vh;
    overflow-y: hidden;
  }

  .hero-showcase {
    position: relative;
    width: 50%;
    padding: 100px 16px 0 16px;
    background: linear-gradient(135deg, #e2cbff, #e2cbff 25%, #deeaff 50%, #ece5ff 75%, #927bce);
  }

  .hero-text {
    padding: 100px 5%;
    width: 50%;
    background-color: black;
  }

  .book-cover {
    position: absolute;
    right: 2%;
    bottom: 0;
    width: 65%;
    transform: translateY(30%);
  }

  .phone-cover {
    position: absolute;
    width: 35%;
    bottom: 0;
    right: 52%;
    transform: translateY(25%);
  }
</style>
