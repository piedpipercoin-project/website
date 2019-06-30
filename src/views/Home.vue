<template>
  <b-container class="home roadmap">
    <b-row class="justify-content-md-center">
      <h1>Pied Piper Road Map</h1>
    </b-row>

    <b-row class="justify-content-md-center">
      <article>
        <h2>
          <font-awesome-icon :icon="['fab', 'pied-piper-hat']" />
          <p>PHASE 1: Introducting Piper Chat</p>
        </h2>
        <div>
          <p>
            We're working on 
            <i>an app</i> that brings together all the show enthusiast 
            (including fans of Erlich who still use Aviato) in one chat app. Your PPI tokens will 
            allow you to chat and interact with other Silicon Valley fans. 
            This one-time fee is designed to curate the potential member's list and make sure 
            that only the geekiest and most enthusiast members of the fanbase gain access.
          </p>
          <p>
            Piperchat for IOS will be
            <i>released during the Q3 of 2019</i>
          </p>
        </div>
      </article>
    </b-row>

    <b-row class="justify-content-md-center">
      <article>
        <h2>
          <font-awesome-icon :icon="['fab', 'pied-piper-hat']" />
          <p>PHASE 2: Piper Chat & FLINT Airdrop</p>
        </h2>
        <div>
          <p>
            Introducing
            <i>Piper Chat</i> will onboard all of our community members from
            Telegram onto Piper Chat, bringing over more than 1000 users.
          </p>
          <p>
            A
            <i>1:1 token airdrop</i> to PPI users will be carried out to both IOS
            and Android holders at the same time. Unlike the last airdrop, the
            amount of FLINT tokens you receive
            will be directly proportional to the PPI tokens you hold.
          </p>
        </div>
      </article>
    </b-row>

    <b-row class="justify-content-md-center">
      <article>
        <h2>
          <font-awesome-icon :icon="['fab', 'pied-piper-hat']" />
          <p>PHASE 3: Hotdog or No Hotdog Battle App</p>
        </h2>
        <div>
          <p>
            <i>Join a battle</i> by staking a certain amount of PPI, then
            compete with other community members in a challenge of determining
            whether or not what you're seeing in the picture is a hotdog.
            Joining a battle requires staking tokens, and if you win you can
            stack some more.
          </p>
        </div>
      </article>
    </b-row>

    <b-row class="justify-content-md-center">
      <article>
        <h2>
          <font-awesome-icon :icon="['fab', 'pied-piper-hat']" />
          <p>PHASE 4: Exchange Raise and Full Chain Fork</p>
        </h2>
        <div>
          <p>In the long run, we are planning to fork PPI off of Ethereum
            and onto a well-developed and trustworthy chain.</p>
        </div>
      </article>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'home'
}
</script>

<style scoped lang="scss">
.roadmap {
  // margin: 0 auto;
  // text-align: left;

  h1 {
    font-size: 50px;
  }

  @media screen and (max-width: 700px) {
    h1 {
      font-size: 30px;
      text-align: center;
      margin: 0 auto;
    }
  }

  article {
    max-width: 700px;
    padding: 20px;

    h2 {
      color: #ffffff;
      line-height: 35px;
      font-size: 23px;
      display: flex;
      flex-direction: row;
      text-transform: uppercase;

      p {
      }

      svg {
        padding-right: 15px;
        color: #217f51;
        font-size: 37px;
      }
    }
    
    div {
      border-left: 3px solid #217f51;
      font-size: 15px;
      line-height: 150%;
      text-transform: none;
      padding: 10px 30px;
      margin: 15px;

      p {
        padding: 10px 0;

        i {
          color: #217f51;
        }
      }
    }

    @media screen and (max-width: 700px) {
      h2 {
        font-size: 20px;
        color: #ffffff;
        line-height: 25px;
        display: flex;
        flex-direction: row;

        p {
        }

        svg {
          padding-right: 15px;
          color: #217f51;
        }
      }

      div {
        border-left: 3px solid #217f51;
        font-size: 15px;
        line-height: 150%;
        text-transform: none;
        padding: 10px 25px;
        margin: 10px;

        p {
          padding: 10px 0;

          i {
            color: #217f51;
          }
        }
      }
    }

    @media screen and (max-width: 550px) {
      h2 {
        font-size: 17x;
        color: #ffffff;
        line-height: 25px;
        display: flex;
        flex-direction: row;

        p {
        }

        svg {
          font-size: 38px;
          padding-right: 15px;
          color: #217f51;
        }
      }

      div {
        border-left: 3px solid #217f51;
        font-size: 15px;
        line-height: 150%;
        text-transform: none;
        padding: 10px 25px;
        margin: 10px;

        p {
          padding: 10px 0;

          i {
            color: #217f51;
          }
        }
      }
    }
  }
}
</style>