<template>
  <div class="vue-2-lame">
    <!-- Feature section with screenshot -->
    <article id="sererless" class="feature">
      <header>
        <h2>Serverless</h2>
        <p>No server? No problem.</p>
        <p>Phasellus lorem quam molestie id quisque diam aenean nulla in. Accumsan in quis quis nunc, ullamcorper malesuada. Eleifend condimentum id viverra nulla.</p>
      </header>
      <img src="https://tailwindui.com/img/component-images/green-project-app-screenshot.jpg"/>
    </article>
    <!-- Feature section with grid -->
    <section id="features">
      <header>
        <h2>Deploy faster</h2>
        <p>Everything you need to deploy your app</p>
        <p>
          Phasellus lorem quam molestie id quisque diam aenean
          nulla in. Accumsan in quis quis nunc, ullamcorper malesuada.
          Eleifend condimentum id viverra nulla.
        </p>
      </header>
      <ul>
        <li v-for="feature in features" :key="feature.name">
          <component :is="feature.icon" aria-hidden="true" />
          <h3>{{ feature.name }}</h3>
          <p>{{ feature.description }}</p>
        </li>
      </ul>
    </section>

    <!-- Testimonial section -->
    <figure id="testimonials">
      <img src="https://images.unsplash.com/photo-1520333789090-1afc82db536a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2102&q=80"/>
      <figcaption>
        <blockquote>
          <svg fill="currentColor" viewBox="0 0 32 32" aria-hidden="true">
            <path d="M9.352 4C4.456 7.456 1 13.12 1 19.36c0 5.088 3.072 8.064 6.624 8.064 3.36 0 5.856-2.688 5.856-5.856 0-3.168-2.208-5.472-5.088-5.472-.576 0-1.344.096-1.536.192.48-3.264 3.552-7.104 6.624-9.024L9.352 4zm16.512 0c-4.8 3.456-8.256 9.12-8.256 15.36 0 5.088 3.072 8.064 6.624 8.064 3.264 0 5.856-2.688 5.856-5.856 0-3.168-2.304-5.472-5.184-5.472-.576 0-1.248.096-1.44.192.48-3.264 3.456-7.104 6.528-9.024L25.864 4z" />
          </svg>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed urna nulla vitae laoreet augue. Amet feugiat est integer dolor auctor adipiscing nunc urna, sit.</p>
          <footer>
            <p>Judith Black</p>
            <p>CEO at PureInsights</p>
          </footer>
        </blockquote>
      </figcaption>
    </figure>

    <!-- Blog section -->
    <section id="articles">
      <header>
        <h2>Learn</h2>
        <p>Helpful Resources</p>
        <p>
          Phasellus lorem quam molestie id quisque diam aenean nulla in.
          Accumsan in quis quis nunc, ullamcorper malesuada. Eleifend
          condimentum id viverra nulla.
        </p>
      </header>
      <article v-for="post in blogPosts" :key="post.id">
        <header>
          <img :src="post.imageUrl"/>
          <a :href="post.category.href">{{ post.category.name }}</a>
        </header>
        <a :href="post.href">
          <p>{{ post.title }}</p>
          <p>{{ post.preview }}</p>
        </a>
        <footer>
          <a :href="post.author.href">
            <img :src="post.author.imageUrl" :alt="post.author.name" />
            <p>{{ post.author.name }}</p>
          </a>
          <time :datetime="post.datetime">{{ post.date }}</time>
          <span aria-hidden="true"> &middot; </span>
          <span> {{ post.readingLength }} read </span>
        </footer>
      </article>
    </section>
  </div>
</template>
