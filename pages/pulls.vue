<template>
  <div class="pulls">
    <div class="content-container">
      <Input />
      <Results />
      <SubInfo />
      <div class="separator" />
      <Footer />
    </div>
  </div>
</template>

<script>
import Input from "@/components/content/pulls/Input";
import Results from "@/components/content/pulls/Results";
import SubInfo from "@/components/content/pulls/SubInfo";
import Footer from "@/components/content/pulls/Footer";
export default {
  layout: "Common",
  components: {
    Input,
    Results,
    SubInfo,
    Footer,
  },
};
</script>

<style lang="scss">
.pulls {
  background: var(--bg-aside);
  padding-bottom: 10rem;
  & .content-container {
    max-width: 980px;
    margin: 0 auto;
  }
  &-top-cage {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 2rem;
    &-filter {
      & ul {
        list-style-type: none;
        display: flex;
        justify-content: center;
        align-items: center;
        & li {
          padding: 5px 15px;
          border: 1px solid var(--border-color);
          &:nth-child(2) {
            border-left: none;
            border-right: none;
          }
          &:first-child {
            border-radius: 6px 0 0 6px;
            background: #1f6feb;
            & a {
              color: var(--white);
            }
          }
          &:last-child {
            border-radius: 0 6px 6px 0;
            border-left: none;
          }
        }
      }
    }
    &-input {
      position: relative;
      &-icon {
        position: absolute;
        top: 8px;
        left: 10px;
      }
      & input {
        background: var(--bg-main);
        border: none;
        border: 1px solid var(--border-color);
        border-radius: 6px;
        width: 560px;
        color: var(--text-primary);
        padding: 5px;
        font-weight: 400;
        line-height: 2rem;
        &:focus {
          outline: none;
        }
        &::placeholder {
          color: var(--text-secondary);
          padding: 0.5rem 3rem;
          font-weight: 400;
          line-height: 2rem;
        }
      }
    }
  }
  &-content {
    border: 1px solid var(--border-color);
    border-radius: 6px;
    margin-top: 1.8rem;
    &-top {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px;
      background: var(--bg-header);
      border-bottom: 1px solid var(--border-color);
      &-left {
        display: flex;
        justify-content: center;
        align-items: center;
        & a {
          display: flex;
          justify-content: center;
          align-items: center;
          flex-wrap: wrap;
          & svg {
            padding-right: 5px;
          }
          &:nth-child(2) {
            color: var(--text-hover);
            font-weight: 400;
            padding-left: 10px;
          }
        }
      }
      &-right {
        & a {
          color: var(--text-hover);
          font-weight: 400;
          padding-left: 30px;
        }
        .dropdown-caret {
          color: var(--text-hover);
        }
      }
    }
    &-bottom {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 8rem 0;
      & h1 {
        font-size: 2.4rem;
        font-weight: 600;
        line-height: 3.6rem;
        padding-top: 3rem;
        padding-bottom: 2rem;
      }
      & p {
        font-size: 1.6rem;
        font-weight: 400;
        line-height: 2.4rem;
        color: var(--text-secondary);
        & a {
          color: var(--blue);
          font-size: 1.6rem;
          font-weight: 400;
          line-height: 2.4rem;
        }
      }
    }
  }
  &-sub-info {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 2rem;
    & p {
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 1.4rem;
      & span {
        padding-left: 5px;
        & strong {
          color: var(--text-primary);
          font-weight: 600;
        }
        & a {
          color: var(--blue);
          font-weight: 400;
        }
      }
    }
  }
  & .separator {
    background: var(--text-hover);
    margin-top: 4rem;
  }
  &-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 3.5rem;
    & ul {
      list-style-type: none;
      display: flex;
      justify-content: center;
      align-items: center;
      & li a {
        padding-left: 30px;
        font-size: 1.2rem;
        font-weight: 400;
        color: var(--blue);
        &:hover {
          text-decoration: underline;
        }
      }
    }
    &-left {
      display: flex;
      justify-content: center;
      align-items: center;
      & a {
        display: flex;
        justify-content: center;
        align-items: center;
        & span {
          margin-left: 1rem;
          font-size: 1.2rem;
          line-height: 1.8rem;
          font-weight: 400;
          color: var(--text-secondary);
        }
      }
    }
  }
}

@media screen and (max-width: 970px) {
  .pulls {
    padding: 0 20px;
    &-top-cage {
      &-input {
        & input {
          width: 400px;
        }
      }
    }
  }
}
@media screen and (max-width: 810px) {
  .pulls {
    &-top-cage {
      &-input {
        & input {
          width: 300px;
        }
      }
    }
  }
}
@media screen and (max-width: 700px) {
  .pulls {
    &-top-cage {
      &-input {
        & input {
          width: 250px;
        }
      }
    }
  }
}
@media screen and (max-width: 543px) {
  .pulls {
    & .content-container {
      max-width: 980px;
      margin: 0 auto;
    }
    &-top-cage {
      flex-direction: column;
      &-filter {
        & ul {
          & li {
            padding: 5px 32px;
            &:nth-child(3) {
              border-radius: 0 6px 6px 0;
            }
            &:last-child {
              display: none;
            }
          }
        }
      }
      &-input {
        margin-top: 1rem;
        & input {
          width: 370px;
        }
      }
    }
    &-content {
      &-top-right {
        display: none;
      }
      &-bottom {
        padding: 8rem 4rem;
        text-align: center;
      }
    }
    &-footer {
      padding-bottom: 3rem;
      & ul {
        display: none;
      }
      &-logo {
        display: none;
      }
    }
  }
}
@media screen and (max-width: 415px) {
  .pulls {
    &-top-cage {
      &-filter {
        & ul {
          & li {
            padding: 5px 25px;
          }
        }
      }
      &-input {
        & input {
          width: 320px;
        }
      }
    }
  }
}
</style>