<template>
  <div>
    <div class="indent">
      <span class="overline">Over De Codebrouwers</span>
      <h1 class="title small">Wie zit erachter?</h1>

      <div class="team">
        <div class="profile">
          <img class="image" src="/vincent-min.jpg" alt="" />

          <div class="description">
            <h2 class="name">Vincent Brouwer</h2>

            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit.
              Pellentesque aliquam sem quis hendrerit mattis. Ut posuere dui
              nibh, vitae dictum lectus vehicula eget. Phasellus tempus id mi
              efficitur mattis. Fusce vel nisi ut metus dapibus fermentum.
              Quisque lacinia sit amet est a sodales. Donec tincidunt vitae sem
              ut convallis. Vivamus orci lacus, mattis vitae ante non, feugiat
              laoreet orci. Curabitur sagittis odio id ex volutpat, auctor
              maximus ligula hendrerit. Donec nec tempus justo, id imperdiet
              lacus. Integer laoreet mauris ante, in rhoncus massa imperdiet
              rhoncus. Aenean tristique sapien at consequat porta. Phasellus
              accumsan magna quis aliquet ultricies. Morbi in magna tortor.
              Vivamus consequat varius lorem sit amet aliquam.
            </p>

            <p>
              Nulla id elementum lacus. Donec justo enim, maximus sit amet
              vehicula in, convallis ac mi. Nulla id volutpat justo, nec
              malesuada justo. Lorem ipsum dolor sit amet, consectetur
              adipiscing elit. Vivamus nisi nibh, sodales pharetra sodales eget,
              tincidunt ac ex. Integer facilisis pharetra venenatis. Nullam
              consectetur finibus nisi, vel volutpat est congue finibus.
              Pellentesque finibus est vel bibendum tempus. Ut tristique erat
              sed dignissim scelerisque.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style lang="scss" scoped>
.team {
  margin-top: 4rem;

  .profile {
    display: flex;
    gap: 2rem;

    .description {
      max-width: 750px;

      .name {
        margin-top: 0;
      }
    }

    .image {
      width: 300px;

      aspect-ratio: 1/1.25;

      object-fit: cover;

      border-radius: var(--main-border-radius);
    }
  }
}
</style>
