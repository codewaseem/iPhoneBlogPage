<template>
  <div class="blog-post">
    <h2 class="blog-post__title">10 Best Photo Apps For Incredible iPhone Photography (2020 Edition)</h2>

    <svg
      class="blog-post__divider"
      width="100%"
      viewBox="0 0 340 2"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M1.47753 1.5H340.522"
        stroke="url(#paint0_linear)"
        stroke-width="2"
        stroke-linecap="square"
      />
      <defs>
        <linearGradient id="paint0_linear" gradientUnits="userSpaceOnUse">
          <stop offset="0.000923775" stop-color="#9B2686" />
          <stop offset="1" stop-color="#E51323" />
        </linearGradient>
      </defs>
    </svg>

    <p>
      How do you capture more interesting travel photos with your iPhone?
      How do you avoid taking the same cliché vacation photos that
      everyone else takes? I recently interviewed Steffen Geldner – a
      talented iPhone photographer with a passion for travel. In this
      article, Steffen reveals 7 tips for shooting beautiful travel photos
      that will preserve the amazing memories of your trip. Read on to
      discover how to take better travel photos with your iPhone!
    </p>

    <img class="blog-post__image" src="../../images/img.jpg" alt />

    <section>
      <h2 class="blog-post__section-heading">
        1. Research Your Destination To Find The Best Photo
        Opportunities
      </h2>

      <p class="blog-post__paragraph">
        Before your trip, I recommend researching the destination to
        find the most interesting photo opportunities.
      </p>

      <p class="blog-post__paragraph">
        I always research the location I’m traveling to. I do this
        extensively and obsessively!
      </p>

      <p class="blog-post__paragraph">
        It’s up to you how much research you do. But you should
        definitely spend a bit of time looking up some great places to
        take pictures.
      </p>
      <p class="blog-post__paragraph">So, what kind of research can you do?</p>
      <p class="blog-post__paragraph">
        First, you could search for photos that other people have taken
        at the locations you’re planning to visit.
      </p>
      <p class="blog-post__paragraph">
        Search on Instagram or Google to get an idea of the kinds of
        photos people take there.
      </p>
    </section>
    <section class="blog-post__section">
      <h2 class="blog-post__section-heading">
        2. Capture Your Journey To Tell The Complete Story Of Your
        Travels
      </h2>

      <p class="blog-post__paragraph">
        Travel photography isn’t just about photographing the
        destination.
      </p>
      <p class="blog-post__paragraph">
        For a more complete photographic story, capture your journey to
        and from the location you’re visiting.
      </p>
      <p class="blog-post__paragraph">
        If you’re traveling by plane, try to get a window seat where you
        have a view of the wing or propeller.
      </p>
      <p class="blog-post__paragraph">
        And of course, you could capture a beautiful aerial view of
        clouds, mountains, or city lights as you’re flying above.
      </p>
      <p class="blog-post__paragraph">
        Your journey will often involve several different types of
        transport. And they all offer great photo opportunities.
      </p>
      <p class="blog-post__paragraph">
        Whether you’re traveling by car, taxi, bus, train, boat, or
        plane, try to capture some interesting photos.
      </p>
    </section>
  </div>
</template>

<script>
export default {
  mounted() {
    console.log("Blog-Post mounted.");
  }
};
</script>

<style lang="scss" scoped>
@import "../../sass/mixins";

.blog-post {
  color: #101010;
  width: 100%;
  max-width: 560px;
  margin: auto;

  > * {
    width: calc(100% - 35px);
    margin: 25px auto;
    font-weight: 300;
    font-size: 16px;
    line-height: 24px;
  }

  @include element("title") {
    font-size: 24px;
    line-height: 29px;
    font-weight: bold;
  }

  @include element("divider") {
    margin-top: 0;
    display: block;
  }

  @include element("paragraph") {
    margin-bottom: 17px;
  }

  @include element("image") {
    margin: 0;
    width: 100%;
  }

  @include element("section-heading") {
    margin-bottom: 16px;
  }
}
</style>
