<template>
  <div class="homepage-banner" :class="{ hidden }">
    <div class="image">
      <img
        srcset="
          /images/25-proud-to-be-mauve.png    1x,
          /images/25-proud-to-be-mauve@2x.png 2x
        "
        src="/images/25-proud-to-be-mauve.png"
        alt="25 years proud to be mauve"
      />
    </div>
    <div class="text">
      Mauve is proud to be celebrating 25 years providing Global Business
      Solutions and Consultancy Services
    </div>
    <div class="actions">
      <a href="#">Learn more</a>
      <button @click="hide">
        <svg role="img" title="Close" viewBox="0 0 46 46">
          <defs></defs>
          <title>modal-close</title>
          <g id="Layer_2" data-name="Layer 2">
            <g id="Layer_6" data-name="Layer 6">
              <circle cx="23" cy="23" r="21" class="cls-1"></circle>
              <path
                d="M23 46a23 23 0 1 1 23-23 23 23 0 0 1-23 23zm0-42a19 19 0 1 0 19 19A19 19 0 0 0 23 4z"
                class="cls-2"
              ></path>
              <path
                transform="rotate(-45 22.998 23.004)"
                d="M21 12.39h4V33.6h-4z"
                class="cls-2"
              ></path>
              <path
                transform="rotate(-45 22.998 23.004)"
                d="M12.39 21H33.6v4H12.39z"
                class="cls-2"
              ></path>
            </g>
          </g>
        </svg>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomepageBanner',
  data() {
    return {
      hidden: false,
    }
  },
  methods: {
    hide() {
      this.hidden = true
    },
  },
}
</script>

<style lang="scss">
html,
body {
  margin: 0;
}

.homepage-banner {
  position: relative;
  top: 0;

  transition: top 0.3s linear;
  background-color: #aeafd7;
  display: flex;
  align-items: center;

  padding: 20px 30px;

  @media (max-width: 693px) {
    align-items: unset;
  }

  &.hidden {
    top: -200px;
  }
}

.image {
  position: relative;
  padding-right: 20px;

  img {
    display: block;
  }

  &::after {
    content: ' ';
    display: block;
    position: absolute;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
    width: 1px;
    height: 34px;
    background-color: white;
  }

  @media (max-width: 693px) {
    padding-top: 8px;

    &::after {
      transform: none;
      top: 11px;
    }
  }

  @media (max-width: 615px) {
    &::after {
      content: none;
    }
  }
}

.text {
  color: #ffffff;
  font-family: 'Roboto Slab';
  font-size: 15px;
  letter-spacing: 0.68px;
  line-height: 28px;
  padding-left: 20px;
  padding-right: 20px;

  @media (max-width: 615px) {
    display: none;
  }
}

.actions {
  display: flex;
  margin-left: auto;
  align-items: center;

  @media (max-width: 693px) {
    align-items: unset;
    padding-top: 8px;
  }

  a {
    display: inline-block;
    border-radius: 20px;
    background-color: #000000;
    color: #ffffff;
    font-family: Gotham;
    font-size: 16px;
    font-weight: 500;
    letter-spacing: 0.72px;
    line-height: 19px;
    text-decoration: none;
    padding: 10px 20px;
    white-space: nowrap;
  }

  button {
    border: none;
    background: none;
    width: 40px;
    height: 40px;
    padding: 0;
    margin-left: 25px;

    svg {
      width: 100%;
      circle {
        opacity: 1;
        fill: white;
      }
      path:nth-of-type(1) {
        fill: white;
      }
      path:nth-of-type(2),
      path:nth-of-type(3) {
        fill: black;
      }
    }
  }

  @media (max-width: 860px) {
    a {
      display: none;
    }
    button {
      margin-left: 0;
    }
  }
}
</style>