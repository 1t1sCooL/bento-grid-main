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
    --pad: 1rem;
    display: flex;
    flex-direction: column;
    border-radius: 0.625rem;
    padding: var(--pad);
    overflow: hidden;
    /* Let grid/flex tracks shrink below the intrinsic width of their images */
    min-width: 0;
  }

  .card img {
    display: block;
    height: auto;
  }

  .card h2 {
    margin: 0;
    font-size: 1.5rem;
    font-weight: 500;
    line-height: 1;
    letter-spacing: -0.02em;
  }

  /* The follower, create-post and AI cards use a larger heading tier on mobile */
  .card--grow h2,
  .card--create h2,
  .card--ai h2 {
    font-size: 1.875rem;
    line-height: 0.95;
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
    gap: 1.5rem;
    padding: 2.5rem 1rem;
  }

  .card--social__title {
    margin: 0;
    font-size: 2.875rem;
    font-weight: 500;
    line-height: 0.935;
    letter-spacing: -0.03em;
    /* Narrow measure reproduces the design's "10x Faster" / "with AI" wrap */
    max-width: 16.5rem;
  }

  .card--social__stars {
    width: 11.5rem;
    max-width: 80%;
    height: auto;
  }

  .card--social__reviews {
    margin: -1rem 0 0;
    font-size: 1.125rem;
    line-height: 1.2;
  }

  /* ---- Manage multiple platforms ---- */
  .card--platforms {
    background-color: var(--White);
    gap: 1rem;
  }

  /* Account cards render at their natural size; the right edge may crop */
  .card--platforms__img {
    width: 316px;
    max-width: none;
    height: auto;
  }

  /* ---- Consistent schedule ---- */
  .card--schedule-consistent {
    background-color: var(--Yellow500);
    gap: 1.25rem;
  }

  /* Calendar renders at natural size and bleeds off the bottom edge */
  .card--schedule-consistent__img {
    width: 13rem;
    max-width: none;
    height: auto;
    margin: 0 0 -2.25rem;
  }

  /* ---- Schedule to social media ---- */
  .card--schedule-social {
    background-color: var(--Purple100);
    gap: 1.5rem;
    padding: 2rem 1rem;
    text-align: center;
  }

  .card--schedule-social__img {
    width: 100%;
    max-width: 20rem;
    height: auto;
    align-self: center;
  }

  .card--schedule-social p {
    margin: -0.375rem 0 0;
    font-size: 1.125rem;
    line-height: 1.2;
  }

  /* ---- Grow followers ---- */
  .card--grow {
    --pad: 1.5rem;
    background-color: var(--Purple500);
    color: var(--White);
    gap: 2.5rem;
    align-items: center;
    text-align: center;
  }

  /* Narrow measure forces the three-line wrap from the design */
  .card--grow h2 {
    max-width: 13rem;
  }

  .card--grow__img {
    width: 14.25rem;
    max-width: none;
    height: auto;
  }

  /* ---- Audience growth ---- */
  .card--audience {
    --pad: 1.5rem;
    background-color: var(--White);
    gap: 0;
  }

  /* h2 in the selector so this outranks the shared `.card h2` font size */
  h2.card--audience__stat {
    font-size: 2.875rem;
    line-height: 1;
    letter-spacing: -0.05em;
    margin-bottom: 0.625rem;
  }

  .card--audience__label {
    margin: 0 0 1.5rem;
    font-size: 1.125rem;
    line-height: 1.2;
  }

  .card--audience__img {
    width: 11.1875rem;
    max-width: none;
    height: auto;
    align-self: flex-start;
  }

  /* ---- Create and schedule content ---- */
  .card--create {
    --pad: 2rem;
    background-color: var(--Yellow100);
    gap: 1.5rem;
  }

  /* Slightly tighter tracking so "Create and schedule" fits one line, as designed */
  .card--create h2 {
    letter-spacing: -0.03em;
  }

  .card--create__img {
    width: 11.9375rem;
    max-width: none;
    height: auto;
  }

  /* ---- Write content using AI ---- */
  .card--ai {
    --pad: 1.5rem;
    background-color: var(--Yellow500);
    gap: 1.5rem;
  }

  .card--ai__img {
    width: 13.75rem;
    max-width: none;
    height: auto;
  }

  /* ---- Tablet layout: two balanced columns, mobile-sized card internals ---- */
  @media (min-width: 768px) and (max-width: 1151.98px) {
    .grid {
      grid-template-columns: repeat(2, 1fr);
      grid-template-areas:
        "social           social"
        "platforms        schedule-consistent"
        "schedule-social  schedule-social"
        "grow             ai"
        "audience         create";
    }

    .card--create { grid-area: create; }
    .card--social { grid-area: social; }
    .card--platforms { grid-area: platforms; }
    .card--schedule-consistent { grid-area: schedule-consistent; }
    .card--schedule-social { grid-area: schedule-social; }
    .card--audience { grid-area: audience; }
    .card--grow { grid-area: grow; }
    .card--ai { grid-area: ai; }

    /* The full-width hero can afford desktop-sized type */
    .card--social {
      padding: 3rem;
    }

    .card--social__title {
      font-size: 3.75rem;
      line-height: 3.625rem;
      max-width: none;
      text-wrap: balance;
    }

    /* Cards paired with a taller neighbour centre their content */
    .card--platforms,
    .card--audience {
      justify-content: center;
    }

    /* Calendar sits centred in the wider tablet card */
    .card--schedule-consistent__img {
      align-self: center;
    }

    /* Chat illustration sits on the bottom padding of the stretched card */
    .card--ai__img {
      margin-top: auto;
    }
  }

  /* ---- Desktop bento layout ---- */
  @media (min-width: 1152px) {
    .grid {
      grid-template-columns: repeat(4, 1fr);
      /* Row tracks match the design's 327/58/156/248 grid at 1440; minmax lets
         them grow on narrower viewports where the columns get tighter */
      grid-template-rows:
        minmax(327px, auto) minmax(58px, auto)
        minmax(156px, auto) minmax(248px, auto);
      grid-template-areas:
        "create  social      social            schedule-social"
        "create  platforms   schedule-consistent  schedule-social"
        "ai      platforms   schedule-consistent  schedule-social"
        "ai      audience    grow              grow";
    }

    .card {
      --pad: 1.5rem;
    }

    .card--create { grid-area: create; }
    .card--social { grid-area: social; }
    .card--platforms { grid-area: platforms; }
    .card--schedule-consistent { grid-area: schedule-consistent; }
    .card--schedule-social { grid-area: schedule-social; }
    .card--audience { grid-area: audience; }
    .card--grow { grid-area: grow; }
    .card--ai { grid-area: ai; }

    .card h2 {
      font-size: 1.875rem;
      line-height: 0.935;
    }

    .card--create h2,
    .card--ai h2 {
      font-size: 2.125rem;
      line-height: 1.1;
    }

    .card--create h2 {
      letter-spacing: -0.02em;
    }

    .card--grow h2 {
      font-size: 2.375rem;
      line-height: 1;
      max-width: none;
    }

    .card--social {
      padding: 3rem;
    }

    .card--social__title {
      font-size: 3.75rem;
      line-height: 3.625rem;
      max-width: none;
    }

    .card--platforms {
      gap: 1.125rem;
    }

    .card--schedule-consistent {
      gap: 1rem;
    }

    .card--schedule-social {
      padding: 3rem 2rem;
      gap: 1.75rem;
      text-align: left;
    }

    .card--schedule-social p {
      margin: -0.375rem 0 0;
      font-size: 1.0625rem;
      line-height: 1.2;
    }

    h2.card--audience__stat {
      font-size: 3.75rem;
      line-height: 1;
      margin-bottom: 0.75rem;
    }

    .card--audience__label {
      margin: 0 0 2.25rem;
    }

    .card--create {
      --pad: 2rem;
      gap: 1.25rem;
      justify-content: center;
    }

    /* On desktop the follower card places art beside the copy */
    .card--grow {
      flex-direction: row;
      align-items: center;
      text-align: left;
      gap: 0.75rem;
    }

    /* --- Illustrations render at their natural @2x scale, anchored to the
       card padding; wider ones crop against the card's right edge --- */

    /* Account cards: natural 316px, left-aligned, cropped on the right */
    .card--platforms__img {
      width: 19.75rem;
      max-width: none;
      margin: 0;
      align-self: flex-start;
    }

    /* Calendar: natural 208px, left-aligned; the margin removes its full
       height from layout so the row track sets the card height and the
       calendar clips against the card's bottom edge */
    .card--schedule-consistent__img {
      width: 13rem;
      max-width: none;
      align-self: flex-start;
      margin: 0 0 -11.3125rem;
    }

    /* Best-time chart: natural 357.5px, left-aligned, cropped on the right */
    .card--schedule-social__img {
      width: 357.5px;
      max-width: none;
      align-self: flex-start;
      margin: 0;
    }

    /* Chat: natural 220px, pushed to the card bottom padding */
    .card--ai__img {
      margin-top: auto;
    }

    /* Follower-growth chart: natural 228px, beside the copy at the top padding;
       the tiny negative margin keeps its 201.07px height from inflating the
       248px row track */
    .card--grow__img {
      align-self: flex-start;
      margin: 0 0 -0.125rem;
    }
  }
</style>
