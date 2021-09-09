<template>
  <div>
    <Header />
    <Aside :isShowMobileMenu="isShowMobileMenu" />
    <div class="content">
      <RepoList />
      <Explore />
    </div>
  </div>
</template>

<script>
import RepoList from "@/components/content/homepage/RepoList";
import Explore from "@/components/content/homepage/Explore";
import Header from "@/components/common/Header";
import Aside from "@/components/common/Aside";
export default {
  components: {
    Header,
    Aside,
    Explore,
    RepoList,
  },
};
</script>

<style lang="scss">
.content {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  position: fixed;
  right: 0;
  overflow-y: scroll;
  background: var(--bg-main);
  width: 77%;
  height: 100vh;
  padding: 30px 50px;
  padding-bottom: 15rem;
  &-left {
    width: 65%;
    & h1 {
      font-size: 1.6rem;
      line-height: 2.4rem;
    }
    &-repo {
      margin-top: 2.5rem;
      &-title {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        & img {
          width: 32px;
          height: 32px;
          border-radius: 50%;
          margin-right: 1rem;
        }
        & h2 {
          display: flex;
          align-items: flex-end;
          color: var(--white);
          font-size: 1.4rem;
          line-height: 2.1rem;
          font-weight: 400;
          & a {
            color: var(--white);
            margin: 0 0.5rem;
            &:hover {
              color: var(--blue);
            }
          }
          & span {
            color: var(--text-secondary);
            font-size: 1.2rem;
            line-height: 2.1rem;
            font-weight: 400;
            margin-left: 1rem;
          }
        }
      }
      &-box {
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        background: var(--bg-aside);
        border-radius: 1rem;
        padding: 15px 20px;
        margin: 10px 40px;
        border: 1px solid var(--border-color);
        &-title {
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: flex-start;
          & a {
            font-size: 1.6rem;
            line-height: 2rem;
            color: var(--text-primary);
            &:hover {
              color: var(--blue);
            }
          }
          & p {
            font-size: 1.4rem;
            line-height: 2.1rem;
            padding: 5px 0;
          }
          &-sub {
            display: flex;
            justify-content: center;
            align-items: center;
            & h1 {
              display: flex;
              justify-content: center;
              align-items: center;
              font-size: 1.2rem;
              color: var(--text-secondary);
            }
            & .stars {
              margin: 0 2rem;
              display: flex;
              justify-content: center;
              align-items: center;
              &:hover {
                span {
                  color: var(--blue);
                }
                svg {
                  fill: var(--blue);
                }
              }
              & span {
                font-size: 1.2rem;
                font-weight: 400;
                line-height: 1.8rem;
                color: var(--text-secondary);
                margin-left: 3px;
              }
            }
          }
        }
        &-button {
          & a {
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 4px 12px;
            & span {
              margin-left: 3px;
            }
          }
        }
      }
    }
    & .more-button {
      margin-top: 2rem;
      width: 100%;
      padding: 0.6rem;
      background: var(--bg-aside);
      border-radius: 1rem;
      border: 1px solid #30363d;
      text-align: center;
      & a {
        color: var(--blue);
      }
      &:hover {
        background: #161b22;
      }
    }
    &-footer {
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;
      margin-top: 2rem;
      p,
      .subscribe {
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 1.2rem;
        font-weight: 400;
        line-height: 1.8rem;
        color: var(--text-secondary);
        & span {
          margin-left: 3px;
        }
        & a {
          color: var(--blue);
          &:hover {
            text-decoration: underline;
          }
        }
      }
      .subscribe {
        margin-top: 1rem;
        &:hover {
          color: var(--blue);
          text-decoration: underline;
        }
      }
      &-sub {
        display: flex;
        margin-top: 4rem;
        &-logo a {
          display: flex;
          justify-content: center;
          align-items: center;
          & svg:hover {
            fill: #c9d1d9;
          }
          & span {
            margin-left: 1rem;
            font-size: 1.2rem;
            line-height: 1.8rem;
            font-weight: 400;
            color: var(--text-secondary);
          }
        }
        &-links {
          display: flex;
          justify-content: center;
          align-items: flex-start;
          margin-left: 15rem;
          & .links-box {
            list-style-type: none;
            padding-right: 2.5rem;
            & li {
              padding: 2px 0;
              & a {
                font-size: 1.2rem;
                line-height: 1.8rem;
                font-weight: 400;
                color: var(--text-secondary);
                &:hover {
                  color: var(--blue);
                  text-decoration: underline;
                }
              }
            }
          }
        }
      }
    }
  }
  &-right {
    width: 35%;
    padding: 0 30px;
    padding-top: 2rem;
    & h1 {
      font-size: 1.4rem;
      font-weight: 600;
      line-height: 2.1rem;
      color: var(--text-primary);
    }
    &-explore {
      margin-top: 2rem;
      &-box {
        margin-top: 2rem;

        & a {
          font-size: 1.2rem;
          font-weight: 600;
          line-height: 1.8rem;
          color: var(--text-primary);
          &:hover {
            color: var(--blue);
          }
        }
        & p {
          font-size: 1.2rem;
          font-weight: 400;
          line-height: 1.8rem;
          color: #8b949e;
          padding: 5px 0;
        }
        &-footer {
          display: flex;
          justify-content: flex-start;
          align-items: center;
          margin-top: 1rem;
          & h1 {
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.2rem;
            font-weight: 400;
            line-height: 1.8rem;
            color: #8b949e;
          }
          & a {
            margin: 0 2rem;
            display: flex;
            justify-content: center;
            align-items: center;
            &:hover {
              span {
                color: var(--blue);
              }
              svg {
                fill: var(--blue);
              }
            }
            & span {
              font-size: 1.2rem;
              font-weight: 400;
              line-height: 1.8rem;
              color: #8b949e;
              margin-left: 3px;
            }
          }
        }
      }
    }
  }
}

@media screen and (max-width: 970px) {
  .content {
    width: 64%;
    padding: 30px 20px;
    &-left {
      width: 100%;
      &-footer {
        padding-bottom: 10rem;
        &-sub {
          &-logo {
            display: none;
          }
          &-links {
            margin-left: 0;
            & .links-box {
              padding-right: 6rem;
            }
          }
        }
      }
    }
    &-right {
      display: none;
    }
  }
}
@media screen and (max-width: 700px) {
  .content {
    width: 100%;
    &-left {
      &-repo {
        &-box {
          margin: 10px 10px;
        }
        &-title {
          & h2 {
            flex-wrap: wrap;
          }
        }
      }
      &-footer {
        p,
        .subscribe {
          align-items: flex-start;
        }
        & .octicon-light-bulb {
          width: 22px;
          height: 22px;
        }
      }
    }
  }
}
</style>
