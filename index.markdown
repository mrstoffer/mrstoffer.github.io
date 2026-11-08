---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<section id="welcome">
  <div class="container-fluid bg-primary text-light">
    <div class="row justify-content-md-center">
      <div class="col-12 col-md-6 text-center">
        <h1>Hey there, nice to meet you</h1>
        <hr class="my-4"/>
      </div>
    </div>
    <div class="row justify-content-md-center">
      <div class="col-12 col-md-9 text-center">
        <p class="lead">I'm <strong>Christopher</strong>, an <strong>Electrical Engineering BSc</strong> student at <strong>TU Delft</strong>. If it involves a computer, chances are I'm into it. From hardware descriptions to software systems, I enjoy building things and solving problems with code and electronics.</p>
      </div>
    </div>
    <div class="row justify-content-md-center">
      <div class="col-12 col-md-9 text-center mt-4">
        <a href="/about" class="btn btn-outline-light text-light">More about me</a>
      </div>
    </div>
  </div>
</section>

<section id="projects" class="d-none d-lg-block">
  <div class="container-fluid border-top border-primary border-5">
    <div class="row justify-content-md-center">
      <div class="col-8 text-center">
        <h1>Featured Projects</h1>
        <hr class="mt-4"/>
      </div>
      <div class="col-4 text-center">
        <h1>Latest Posts</h1>
        <hr class="mt-4"/>
      </div>
    </div>
  </div>
  <div class="container-fluid pb-0 pt-0">
    <div class="row justify-content-center">
      <div class="col-8">
        {%- if site.posts.size > 0 -%}
        <div class="row justify-content-center">
          {%- for post in site.posts -%}
          <div class="col-6">
            {% include card.html post=post %}
          </div>
          {%- endfor -%}
        </div>
        {%- endif -%}
      </div>
      <div class="col-4">
        {%- if site.posts.size > 0 -%}
          <!-- <div class="row justify-content-center">
            {%- for post in site.posts -%}
            <div class="col-12 col-lg-6 col-xl-4 mb-4">
              {% include card.html post=post %}
            </div>
            {%- endfor -%}
          <div> -->
        <div class="row justify-content-center">
          <div class="list-group list-group-flush mb-4">
            {%- for post in site.posts -%}
            <a href="{{ post.url | relative_url }}" class="list-group-item list-group-item-action">
              <div class="d-flex justify-content-between">
                <h5 class="mb-1"><strong>{{ post.title }}</strong></h5>
                <small>{{ post.date | date: date_format }}</small>
              </div>
              <p class="mb-1">{{ post.excerpt }}</p>
              <!-- <figure>
                <blockquote class="blockquote">
                  <p><a href="{{ post.url | relative_url }}">{{ post.title }}</a></p>
                </blockquote>
                <figcaption class="blockquote-footer">
                  {{ post.date | date: date_format }}
                </figcaption>
              </figure> -->
            </a>
            {%- endfor -%}
          </div>
        </div>
        {%- endif -%}
      </div>
    </div>
  </div>
  <div class="container-fluid">
    <div class="row justify-content-center">
      <div class="col-8 text-center">
        <a id="to-blog" href="/projects" class="btn btn-primary text-light mb-2">View all projects</a> <br/>
        <!-- <a class="rss-subscribe btn btn-outline-primary" href="{{ "/feed.xml" | relative_url }}">Subscribe via RSS</a> -->
      </div>
      <div class="col-4 text-center">
        <a id="to-blog" href="/archive" class="btn btn-primary text-light mb-2">More posts</a> <br/>
        <!-- <a class="rss-subscribe btn btn-outline-primary" href="{{ "/feed.xml" | relative_url }}">Subscribe via RSS</a> -->
      </div>
    </div>
  </div>
</section>
<section id="blog" class="d-block d-lg-none">
<ul class="nav nav-underline my-3 mx-3 justify-content-center" id="nav-tab" role="tablist">
  <li class="nav-item" role="presentation">
    <button class="nav-link active" id="nav-projects-tab" data-bs-toggle="tab" data-bs-target="#nav-projects" type="button" role="tab" aria-controls="nav-projects" aria-selected="true"><h5>Projects</h5></button>
  </li>
  <li class="nav-item" role="presentation">
    <button class="nav-link" id="nav-posts-tab" data-bs-toggle="tab" data-bs-target="#nav-posts" type="button" role="tab" aria-controls="nav-posts" aria-selected="false"><h5>Posts</h5></button>
  </li>
</ul>
<div class="tab-content mx-3 mb-3" id="nav-tabContent">
  <div class="tab-pane fade show active" id="nav-projects" role="tabpanel" aria-labelledby="nav-projects-tab" tabindex="0">
    {%- if site.posts.size > 0 -%}
      {%- for post in site.posts -%}
        {% include card.html post=post %}
      {%- endfor -%}
    {%- endif -%}
  </div>
  <div class="tab-pane fade" id="nav-posts" role="tabpanel" aria-labelledby="nav-posts-tab" tabindex="0">
    {%- if site.posts.size > 0 -%}
      <div class="list-group list-group-flush mb-4">
        {%- for post in site.posts -%}
        <a href="{{ post.url | relative_url }}" class="list-group-item list-group-item-action">
          <div class="d-flex justify-content-between">
            <h5 class="mb-1"><strong>{{ post.title }}</strong></h5>
            <small>{{ post.date | date: date_format }}</small>
          </div>
          <p class="mb-1">{{ post.excerpt }}</p>
          <!-- <figure>
            <blockquote class="blockquote">
              <p><a href="{{ post.url | relative_url }}">{{ post.title }}</a></p>
            </blockquote>
            <figcaption class="blockquote-footer">
              {{ post.date | date: date_format }}
            </figcaption>
          </figure> -->
        </a>
        {%- endfor -%}
      </div>
    </div>
    {%- endif -%}
  </div>
</section>

<!-- <section id="blog">
  <div class="container-fluid border-top border-primary border-5">
    <div class="row justify-content-md-center">
      <div class="col-12 col-md-6 text-center">
        <h1>Latest posts</h1>
        <hr class="mt-4"/>
      </div>
    </div>
  </div>
</section> -->

<style scoped>
section .container-fluid {
  padding-top: 40px;
  padding-bottom: 40px;
  width: 100%;
}

/* #projects > .container-fluid:first-child {
  /* padding-top: 0; */
  /* margin-bottom: 40px; */
} */

.arrowbtn:hover {
  color: var(--bs-light) !important;
}
</style>