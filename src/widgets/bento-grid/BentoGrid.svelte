<script lang="ts">
  import fiveStars from "../../shared/assets/images/illustration-five-stars.webp";
  import multiplePlatforms from "../../shared/assets/images/illustration-multiple-platforms.webp";
  import consistentSchedule from "../../shared/assets/images/illustration-consistent-schedule.webp";
  import schedulePosts from "../../shared/assets/images/illustration-schedule-posts.webp";
  import growFollowers from "../../shared/assets/images/illustration-grow-followers.webp";
  import audienceGrowth from "../../shared/assets/images/illustration-audience-growth.webp";
  import createPost from "../../shared/assets/images/illustration-create-post.webp";
  import aiContent from "../../shared/assets/images/illustration-ai-content.webp";
</script>

<!-- DOM order follows the mobile stacking order; grid-template-areas repositions
     the cards for the desktop bento layout. -->
<section class="grid" aria-label="Social media management features">
  <!-- Social proof hero -->
  <article class="card card--social">
    <h1 class="card--social__title">
      Social Media <span class="accent-yellow">10x</span>
      <em>Faster</em> with AI
    </h1>
    <img class="card--social__stars" src={fiveStars} alt="Five out of five stars" />
    <p class="card--social__reviews">Over 4,000 5-star reviews</p>
  </article>

  <!-- Manage multiple platforms -->
  <article class="card card--platforms">
    <img class="card--platforms__img" src={multiplePlatforms} alt="Rows of social media account cards" />
    <h2>Manage multiple accounts and platforms.</h2>
  </article>

  <!-- Consistent schedule -->
  <article class="card card--schedule-consistent">
    <h2>Maintain a consistent posting schedule.</h2>
    <img class="card--schedule-consistent__img" src={consistentSchedule} alt="A weekly posting calendar" />
  </article>

  <!-- Schedule to social media -->
  <article class="card card--schedule-social">
    <h2>Schedule to social media.</h2>
    <img class="card--schedule-social__img" src={schedulePosts} alt="Chart of the best times to post" />
    <p>Optimize post timings to publish content at the perfect time for your audience.</p>
  </article>

  <!-- Grow followers -->
  <article class="card card--grow">
    <img class="card--grow__img" src={growFollowers} alt="Follower growth statistics" />
    <h2>Grow followers with non-stop content.</h2>
  </article>

  <!-- Audience growth -->
  <article class="card card--audience">
    <h2 class="card--audience__stat">&gt;56%</h2>
    <p class="card--audience__label">faster audience growth</p>
    <img class="card--audience__img" src={audienceGrowth} alt="Illustrated audience avatars" />
  </article>

  <!-- Create and schedule content -->
  <article class="card card--create">
    <h2>Create and schedule content <em class="accent-purple">quicker.</em></h2>
    <img class="card--create__img" src={createPost} alt="A create post button and cursor" />
  </article>

  <!-- Write content using AI -->
  <article class="card card--ai">
    <h2>Write your content using AI.</h2>
    <img class="card--ai__img" src={aiContent} alt="An AI chat writing assistant" />
  </article>
</section>

<style>
  .grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 2rem;
    width: 100%;
    max-width: 1120px;
  }

  /* ---- Shared card styling ---- */
  .card {
    display: flex;
    flex-direction: column;
    border-radius: 0.625rem;
    padding: 1.75rem;
    overflow: hidden;
    /* Let grid/flex tracks shrink below the intrinsic width of their images */
    min-width: 0;
  }

  .card img {
    max-width: 100%;
  }

  .card h2 {
    margin: 0;
    font-size: 1.875rem;
    font-weight: 500;
    line-height: 1;
    letter-spacing: -0.03em;
  }

  em {
    font-style: italic;
    font-weight: 500;
  }

  .accent-yellow {
    color: var(--Yellow500);
  }

  .accent-purple {
    color: var(--Purple500);
  }

  /* ---- Social proof hero ---- */
  .card--social {
    background-color: var(--Purple500);
    color: var(--White);
    align-items: center;
    text-align: center;
    justify-content: center;
    gap: 1.25rem;
    padding: 2.5rem;
  }

  .card--social__title {
    margin: 0;
    font-size: 2.875rem;
    font-weight: 500;
    line-height: 1;
    letter-spacing: -0.03em;
  }

  .card--social__stars {
    width: 12rem;
    max-width: 80%;
    height: auto;
  }

  .card--social__reviews {
    margin: 0;
    font-size: 1.0625rem;
  }

  /* ---- Manage multiple platforms ---- */
  .card--platforms {
    background-color: var(--White);
    gap: 1.5rem;
  }

  .card--platforms__img {
    width: 100%;
    max-width: 20rem;
    height: auto;
  }

  /* ---- Consistent schedule ---- */
  .card--schedule-consistent {
    background-color: var(--Yellow500);
    gap: 1.5rem;
  }

  .card--schedule-consistent__img {
    width: 100%;
    max-width: 22rem;
    height: auto;
  }

  /* ---- Schedule to social media ---- */
  .card--schedule-social {
    background-color: var(--Purple100);
    gap: 1.5rem;
  }

  .card--schedule-social__img {
    width: 100%;
    max-width: 20rem;
    height: auto;
  }

  .card--schedule-social p {
    margin: 0;
    font-size: 1.0625rem;
  }

  /* ---- Grow followers ---- */
  .card--grow {
    background-color: var(--Purple500);
    color: var(--White);
    gap: 1.75rem;
    align-items: center;
    text-align: center;
  }

  .card--grow__img {
    width: 100%;
    max-width: 20rem;
    height: auto;
  }

  /* ---- Audience growth ---- */
  .card--audience {
    background-color: var(--White);
    gap: 0.25rem;
  }

  .card--audience__stat {
    font-size: 3.75rem;
    letter-spacing: -0.05em;
  }

  .card--audience__label {
    margin: 0 0 0.75rem;
    font-size: 1.0625rem;
  }

  .card--audience__img {
    width: 100%;
    max-width: 16rem;
    height: auto;
  }

  /* ---- Create and schedule content ---- */
  .card--create {
    background-color: var(--Yellow100);
    gap: 1.5rem;
  }

  .card--create__img {
    width: 100%;
    max-width: 14rem;
    height: auto;
  }

  /* ---- Write content using AI ---- */
  .card--ai {
    background-color: var(--Yellow500);
    gap: 1.5rem;
  }

  .card--ai__img {
    width: 100%;
    max-width: 20rem;
    height: auto;
  }

  /* ---- Desktop bento layout ---- */
  @media (min-width: 768px) {
    .grid {
      grid-template-columns: repeat(4, 1fr);
      grid-auto-rows: minmax(0, auto);
      grid-template-areas:
        "create  social      social            schedule-social"
        "create  platforms   schedule-consistent  schedule-social"
        "ai      platforms   schedule-consistent  schedule-social"
        "ai      audience    grow              grow";
    }

    .card--create { grid-area: create; }
    .card--social { grid-area: social; }
    .card--platforms { grid-area: platforms; }
    .card--schedule-consistent { grid-area: schedule-consistent; }
    .card--schedule-social { grid-area: schedule-social; }
    .card--audience { grid-area: audience; }
    .card--grow { grid-area: grow; }
    .card--ai { grid-area: ai; }

    .card--social__title {
      font-size: 3.375rem;
    }

    /* On desktop the follower card places art beside the copy */
    .card--grow {
      flex-direction: row;
      align-items: center;
      text-align: left;
    }

    .card--grow__img {
      width: 55%;
      max-width: 22rem;
    }
  }
</style>
