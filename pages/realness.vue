<template>
  <body>
    <header>
      <nav>
        <a href="#">
          <span>Workflow</span>
          <img src="https://tailwindui.com/img/logos/workflow-mark-teal-200-cyan-400.svg"/>
          <img src="https://tailwindui.com/img/logos/workflow-mark-teal-500-cyan-600.svg"/>
        </a>
        <a v-for="item in navigation" :key="item.name" :href="item.href">
          {{ item.name }}
        </a>
        <a href="#"> sign in </a>
      </nav>
    </header>
    <main>
      <!-- Make some humble claims -->
      <section id="hero">
        <header>
          <a href="#">
            <span>We're hiring</span>
            <span>Visit our careers page</span>
            <ChevronRightIcon aria-hidden="true" />
          </a>
          <h1>
            <span>A better way to</span>
            <span>ship web apps</span>
          </h1>
          <p>Anim aute id magna aliqua ad ad non deserunt sunt. Qui irure qui Lorem cupidatat commodo. Elit sunt amet fugiat veniam occaecat fugiat.</p>
          <form action="#">
            <fieldset>
              <label for="email">Email address</label>
              <input id="email" type="email" placeholder="Enter your email"/>
            </fieldset>
            <button type="submit">Start free trial</button>
            <p>
              Start your free 14-day trial, no credit card necessary.
              By providing your email, you agree to our <a href="#">terms of service</a>.
            </p>
          </form>
        </header>
        <!-- Illustration taken from Lucid Illustrations: https://lucid.pixsellz.io/ -->
        <img src="https://tailwindui.com/img/component-images/cloud-illustration-teal-cyan.svg" />
      </section>

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

      <!-- CTA Section -->
      <figure id="cash-app-patreon">
        <img src="https://images.unsplash.com/photo-1525130413817-d45c1d127c42?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1920&q=60&sat=-100"/>
        <figcaption>
          <h2>Award winning support</h2>
          <p>We’re here to help</p>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Et, egestas tempus tellus etiam sed. Quam a scelerisque amet ullamcorper eu enim et fermentum, augue. Aliquet amet volutpat quisque ut interdum tincidunt duis.</p>
          <nav>
            <a href="#">
              Visit the help center
              <ExternalLinkIcon aria-hidden="true" />
            </a>
          </nav>
        </figcaption>
      </figure>
    </main>
    <footer>
      <h2 id="footer-heading">Footer</h2>
      <div>
        <div>
          <div>
            <img src="https://tailwindui.com/img/logos/workflow-mark-gray-300.svg" alt="Company name" />
            <p>Making the world a better place through constructing elegant hierarchies.</p>
            <div>
              <a v-for="item in footerNavigation.social" :key="item.name" :href="item.href">
                <span>{{ item.name }}</span>
                <component :is="item.icon" aria-hidden="true" />
              </a>
            </div>
          </div>
          <div>
            <div>
              <div>
                <h3>Solutions</h3>
                <ul role="list">
                  <li v-for="item in footerNavigation.solutions" :key="item.name">
                    <a :href="item.href">
                      {{ item.name }}
                    </a>
                  </li>
                </ul>
              </div>
              <div>
                <h3>Support</h3>
                <ul role="list">
                  <li v-for="item in footerNavigation.support" :key="item.name">
                    <a :href="item.href">
                      {{ item.name }}
                    </a>
                  </li>
                </ul>
              </div>
            </div>
            <div>
              <div>
                <h3>Company</h3>
                <ul>
                  <li v-for="item in footerNavigation.company" :key="item.name">
                    <a :href="item.href">
                      {{ item.name }}
                    </a>
                  </li>
                </ul>
              </div>
              <div>
                <h3>Legal</h3>
                <ul>
                  <li v-for="item in footerNavigation.legal" :key="item.name">
                    <a :href="item.href">
                      {{ item.name }}
                    </a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
        <div>
          <p>&copy; 2020 Workflow, Inc. All rights reserved.</p>
        </div>
      </div>
    </footer>
  </body>
</template>
<script setup>
  import {
    CloudUploadIcon,
    CogIcon,
    LockClosedIcon,
    RefreshIcon,
    ServerIcon,
    ShieldCheckIcon
  } from '@heroicons/vue/outline'
  import { ChevronRightIcon, ExternalLinkIcon } from '@heroicons/vue/solid'
  const navigation = [
    { name: 'Product', href: '#' },
    { name: 'Features', href: '#' },
    { name: 'Marketplace', href: '#' },
    { name: 'Company', href: '#' },
  ]
  const features = [
    {
      name: 'Push to Deploy',
      description: 'Ac tincidunt sapien vehicula erat auctor pellentesque rhoncus. Et magna sit morbi vitae lobortis.',
      icon: CloudUploadIcon,
    },
    {
      name: 'SSL Certificates',
      description: 'Qui aut temporibus nesciunt vitae dicta repellat sit dolores pariatur. Temporibus qui illum aut.',
      icon: LockClosedIcon,
    },
    {
      name: 'Simple Queues',
      description: 'Rerum quas incidunt deleniti quaerat suscipit mollitia. Amet repellendus ut odit dolores qui.',
      icon: RefreshIcon,
    },
    {
      name: 'Advanced Security',
      description: 'Ullam laboriosam est voluptatem maxime ut mollitia commodi. Et dignissimos suscipit perspiciatis.',
      icon: ShieldCheckIcon,
    },
    {
      name: 'Powerful API',
      description:
        'Ab a facere voluptatem in quia corrupti veritatis aliquam. Veritatis labore quaerat ipsum quaerat id.',
      icon: CogIcon,
    },
    {
      name: 'Database Backups',
      description: 'Quia qui et est officia cupiditate qui consectetur. Ratione similique et impedit ea ipsum et.',
      icon: ServerIcon,
    },
  ]
  const blogPosts = [
    {
      id: 1,
      title: 'Boost your conversion rate',
      href: '#',
      date: 'Mar 16, 2020',
      datetime: '2020-03-16',
      category: { name: 'Article', href: '#' },
      imageUrl:
        'https://images.unsplash.com/photo-1496128858413-b36217c2ce36?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1679&q=80',
      preview:
        'Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto accusantium praesentium eius, ut atque fuga culpa, similique sequi cum eos quis dolorum.',
      author: {
        name: 'Roel Aufderehar',
        imageUrl:
          'https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80',
        href: '#',
      },
      readingLength: '6 min',
    },
    {
      id: 2,
      title: 'How to use search engine optimization to drive sales',
      href: '#',
      date: 'Mar 10, 2020',
      datetime: '2020-03-10',
      category: { name: 'Video', href: '#' },
      imageUrl:
        'https://images.unsplash.com/photo-1547586696-ea22b4d4235d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1679&q=80',
      preview:
        'Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit facilis asperiores porro quaerat doloribus, eveniet dolore. Adipisci tempora aut inventore optio animi., tempore temporibus quo laudantium.',
      author: {
        name: 'Brenna Goyette',
        imageUrl:
          'https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80',
        href: '#',
      },
      readingLength: '4 min',
    },
    {
      id: 3,
      title: 'Improve your customer experience',
      href: '#',
      date: 'Feb 12, 2020',
      datetime: '2020-02-12',
      category: { name: 'Case Study', href: '#' },
      imageUrl:
        'https://images.unsplash.com/photo-1492724441997-5dc865305da7?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1679&q=80',
      preview:
        'Lorem ipsum dolor sit amet consectetur adipisicing elit. Sint harum rerum voluptatem quo recusandae magni placeat saepe molestiae, sed excepturi cumque corporis perferendis hic.',
      author: {
        name: 'Daniela Metz',
        imageUrl:
          'https://images.unsplash.com/photo-1487412720507-e7ab37603c6f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80',
        href: '#',
      },
      readingLength: '11 min',
    },
  ]
  const footerNavigation = {
    solutions: [
      { name: 'Marketing', href: '#' },
      { name: 'Analytics', href: '#' },
      { name: 'Commerce', href: '#' },
      { name: 'Insights', href: '#' },
    ],
    support: [
      { name: 'Documentation', href: '#' },
      { name: 'Guides', href: '#' }
    ],
    company: [
      { name: 'About', href: '#' },
      { name: 'Blog', href: '#' },
    ],
    legal: [
      { name: 'Claim', href: '#' },
      { name: 'Privacy', href: '#' },
      { name: 'Terms', href: '#' }
    ]
  }
</script>
