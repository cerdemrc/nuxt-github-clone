<template>
  <div class="header">
    <div class="container">
      <div class="header-content">
        <div class="header-content-left">
          <div class="header-content-left-logo">
            <nuxt-link to="/">
              <svg
                height="32"
                aria-hidden="true"
                viewBox="0 0 16 16"
                version="1.1"
                width="32"
                fill="#F0F6FC"
                data-view-component="true"
                class="octicon octicon-mark-github v-align-middle"
              >
                <path
                  fill-rule="evenodd"
                  d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"
                ></path></svg
            ></nuxt-link>
          </div>
          <div class="input-cage">
            <input type="text" placeholder="Search or jump to..." />
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="22"
              height="20"
              aria-hidden="true"
              class="mr-1 header-search-key-slash"
            >
              <path
                fill="none"
                stroke="#979A9C"
                opacity=".4"
                d="M3.5.5h12c1.7 0 3 1.3 3 3v13c0 1.7-1.3 3-3 3h-12c-1.7 0-3-1.3-3-3v-13c0-1.7 1.3-3 3-3z"
              ></path>
              <path fill="#979A9C" d="M11.8 6L8 15.1h-.9L10.8 6h1z"></path>
            </svg>
          </div>
          <div class="header-content-left-links">
            <ul>
              <li><nuxt-link to="/pulls" tag="a">Pull requests</nuxt-link></li>
              <li><nuxt-link to="/issues" tag="a">Issues</nuxt-link></li>
              <li>
                <nuxt-link to="/marketplace" tag="a">Marketplace</nuxt-link>
              </li>
              <li><nuxt-link to="/explore" tag="a">Explore</nuxt-link></li>
            </ul>
          </div>
        </div>
        <div class="header-content-right">
          <div
            class="header-content-right-notification"
            title="You have unread notifications"
          >
            <a href="#">
              <svg
                aria-hidden="true"
                height="16"
                viewBox="0 0 16 16"
                version="1.1"
                width="16"
                fill="#F0F6FC"
                data-view-component="true"
                class="octicon octicon-bell"
              >
                <path
                  d="M8 16a2 2 0 001.985-1.75c.017-.137-.097-.25-.235-.25h-3.5c-.138 0-.252.113-.235.25A2 2 0 008 16z"
                ></path>
                <path
                  fill-rule="evenodd"
                  d="M8 1.5A3.5 3.5 0 004.5 5v2.947c0 .346-.102.683-.294.97l-1.703 2.556a.018.018 0 00-.003.01l.001.006c0 .002.002.004.004.006a.017.017 0 00.006.004l.007.001h10.964l.007-.001a.016.016 0 00.006-.004.016.016 0 00.004-.006l.001-.007a.017.017 0 00-.003-.01l-1.703-2.554a1.75 1.75 0 01-.294-.97V5A3.5 3.5 0 008 1.5zM3 5a5 5 0 0110 0v2.947c0 .05.015.098.042.139l1.703 2.555A1.518 1.518 0 0113.482 13H2.518a1.518 1.518 0 01-1.263-2.36l1.703-2.554A.25.25 0 003 7.947V5z"
                ></path>
              </svg>
            </a>
            <div class="notification-circle"></div>
          </div>
          <div class="header-content-right-plus">
            <a href="#">
              <svg
                aria-hidden="true"
                height="16"
                viewBox="0 0 16 16"
                version="1.1"
                fill="#F0F6FC"
                width="16"
                data-view-component="true"
                class="octicon octicon-plus"
              >
                <path
                  fill-rule="evenodd"
                  d="M7.75 2a.75.75 0 01.75.75V7h4.25a.75.75 0 110 1.5H8.5v4.25a.75.75 0 11-1.5 0V8.5H2.75a.75.75 0 010-1.5H7V2.75A.75.75 0 017.75 2z"
                ></path>
              </svg>
            </a>
            <span class="dropdown-caret"></span>
          </div>
          <div class="header-content-right-profile">
            <img src="@/assets/image/profile.jpeg" />
            <span class="dropdown-caret"></span>
          </div>
        </div>
      </div>
    </div>
    <div class="header-mobile">
      <div class="header-mobile-logos">
        <a href="#" @click="openMobileMenu"
          ><svg
            aria-hidden="true"
            height="24"
            viewBox="0 0 16 16"
            version="1.1"
            width="24"
            fill="#F0F6FC"
            data-view-component="true"
            class="octicon octicon-three-bars"
          >
            <path
              fill-rule="evenodd"
              d="M1 2.75A.75.75 0 011.75 2h12.5a.75.75 0 110 1.5H1.75A.75.75 0 011 2.75zm0 5A.75.75 0 011.75 7h12.5a.75.75 0 110 1.5H1.75A.75.75 0 011 7.75zM1.75 12a.75.75 0 100 1.5h12.5a.75.75 0 100-1.5H1.75z"
            ></path>
          </svg>
        </a>
        <nuxt-link to="/" tag="a">
          <svg
            height="32"
            aria-hidden="true"
            viewBox="0 0 16 16"
            version="1.1"
            width="32"
            fill="#F0F6FC"
            data-view-component="true"
            class="octicon octicon-mark-github v-align-middle"
          >
            <path
              fill-rule="evenodd"
              d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"
            ></path></svg
        ></nuxt-link>
        <a href="#"
          ><svg
            aria-hidden="true"
            height="16"
            viewBox="0 0 16 16"
            version="1.1"
            width="16"
            fill="#F0F6FC"
            data-view-component="true"
            class="octicon octicon-bell"
          >
            <path
              d="M8 16a2 2 0 001.985-1.75c.017-.137-.097-.25-.235-.25h-3.5c-.138 0-.252.113-.235.25A2 2 0 008 16z"
            ></path>
            <path
              fill-rule="evenodd"
              d="M8 1.5A3.5 3.5 0 004.5 5v2.947c0 .346-.102.683-.294.97l-1.703 2.556a.018.018 0 00-.003.01l.001.006c0 .002.002.004.004.006a.017.017 0 00.006.004l.007.001h10.964l.007-.001a.016.016 0 00.006-.004.016.016 0 00.004-.006l.001-.007a.017.017 0 00-.003-.01l-1.703-2.554a1.75 1.75 0 01-.294-.97V5A3.5 3.5 0 008 1.5zM3 5a5 5 0 0110 0v2.947c0 .05.015.098.042.139l1.703 2.555A1.518 1.518 0 0113.482 13H2.518a1.518 1.518 0 01-1.263-2.36l1.703-2.554A.25.25 0 003 7.947V5z"
            ></path>
          </svg>
        </a>
      </div>
    </div>
    <div class="aside-mobile" v-if="isShowMenu">
      <div class="aside-mobile-content">
        <input type="text" placeholder="Search GitHub" />
        <div class="separator" />
        <div class="aside-mobile-content-links">
          <ul>
            <li><nuxt-link to="/" tag="a">Dashboard</nuxt-link></li>
            <div class="li-separator" />
            <li><nuxt-link to="/pulls" tag="a">Pull requests</nuxt-link></li>
            <div class="li-separator" />
            <li><a href="#">Issues</a></li>
            <div class="li-separator" />
            <li><a href="#">Marketplace</a></li>
            <div class="li-separator" />
            <li><a href="#">Explore</a></li>
            <div class="li-separator" />
            <li><a href="#">Codespaces</a></li>
            <div class="li-separator" />
            <li><a href="#">Sponsors</a></li>
            <div class="li-separator" />
            <li><a href="#">Settings</a></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isShowMenu: false,
    };
  },
  methods: {
    openMobileMenu() {
      this.isShowMenu = !this.isShowMenu;
    },
  },
};
</script>

<style lang="scss">
.container {
  max-width: 1800px;
  margin: 0 auto;
}
.header {
  background: var(--bg-header);
  padding: 1.6rem;
  font-size: 1.4rem;
  &-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    &-left {
      display: flex;
      justify-content: center;
      align-items: center;
      &-logo {
        margin-right: 1.6rem;
        flex-wrap: nowrap;
      }
      & input {
        margin-right: 1rem;
        background: var(--bg-aside);
        border: none;
        border: 1px solid var(--border-color);
        border-radius: 6px;
        width: 260px;
        max-width: 100%;
        color: var(--text-primary);
        padding: 5px;
        font-weight: 400;
        line-height: 2rem;
        &:focus {
          outline: none;
        }
        &::placeholder {
          color: var(--text-primary);
          padding: 5px;
          font-weight: 400;
          line-height: 2rem;
        }
      }
      & .input-cage {
        position: relative;
        & svg {
          position: absolute;
          right: 12px;
          top: 6px;
        }
      }
      &-links {
        & ul {
          display: flex;
          list-style-type: none;
          & li a {
            color: var(--white);
            margin-left: 2rem;
            white-space: nowrap;
            &:hover {
              color: var(--text-hover);
            }
          }
        }
      }
    }
    &-right {
      display: flex;
      justify-content: center;
      align-items: center;
      & .dropdown-caret {
        display: inline-block;
        color: var(--white);
        width: 0;
        height: 0;
        vertical-align: middle;
        content: "";
        border-style: solid;
        border-width: 4px 4px 0;
        border-right-color: transparent;
        border-bottom-color: transparent;
        border-left-color: transparent;
      }
      &-notification {
        margin-right: 1.6rem;
        position: relative;
        & svg:hover {
          fill: var(--text-hover);
        }
        & .notification-circle {
          position: absolute;
          top: -5px;
          right: -3px;
          width: 10px;
          height: 10px;
          border-radius: 50%;
          background: #2787f6;
        }
      }
      &-plus {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-right: 1.6rem;
        & span {
          margin-left: 3px;
          &:hover {
            cursor: pointer;
          }
        }
        &:hover {
          & svg {
            fill: var(--text-hover);
          }
          & span {
            color: var(--text-hover);
          }
        }
      }
      &-profile {
        display: flex;
        justify-content: center;
        align-items: center;
        &:hover {
          cursor: pointer;
          & span {
            color: var(--text-hover);
          }
        }
        & span {
          margin-left: 5px;
        }
        & img {
          width: 20px;
          height: 20px;
          border-radius: 50%;
        }
      }
    }
  }
  &-mobile {
    display: none;
  }
}

@media screen and (max-width: 820px) {
  .header {
    padding: 1.6rem;
    &-content {
      display: none;
    }
    &-mobile {
      display: block;
      &-logos {
        display: flex;
        align-items: center;
        justify-content: space-between;
      }
    }
  }
}
</style>