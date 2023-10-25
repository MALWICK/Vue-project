<template>
  <div>
    <div class="container">
      <div class="innercontainer">
        <div class="popup">
          <div class="header">
            <h2>This App will be added to your List of Installed Apps</h2>
          </div>
          <div class="innercont">
            <h3>
              <span class="attention">First! </span> Provide your User Inforamtion for this Platform
            </h3>
            <form>
              <div class="first__row">
                <div class="left__cont">
                  <span class="label">First Name</span>
                  <div class="input__holder">
                    <input
                      type="text"
                      class="first__name"
                      placeholder="Enter your first name"
                      value="Bata"
                    />
                  </div>
                </div>
                <div class="right__cont">
                  <span class="label">Last Name</span>
                  <div class="input__holder">
                    <input
                      type="text"
                      class="first__name"
                      placeholder="Enter your last Name"
                      value="Humphrey"
                    />
                  </div>
                </div>
              </div>
              <div class="fullrow">
                <div class="full__cont">
                  <span class="label">Email Address</span>
                  <div class="fullinput__holder">
                    <input
                      type="email"
                      class="first__name"
                      placeholder="Enter your first name"
                      value="BataHumphrey@gmail.com"
                    />
                  </div>
                </div>
                <div class="apikey__cont">
                  <p class="api__key">
                    <span class="apispan">ApiKey:</span> Mh&resa18903679800387845*****
                  </p>
                  <button class="copy">Copy <i class="fa-solid fa-copy"></i></button>
                </div>
                <div class="confirm">
                  <button>Confirm</button>
                </div>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UsersApplication',

  data() {
    return {
      items: [
        {
          id: 1,
          apptitle: 'Vend',
          logo: 'https://pipedream.com/s.v0/app_mWnhAp/logo/48',
          status: 'Download'
        },
        {
          id: 2,
          apptitle: 'Airtable',
          logo: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSYI0SdC_3xBMmEvh43Dao1SI9Y_n7qqFeSbQ&usqp=CAU',
          status: 'installed'
        },
        {
          id: 3,
          apptitle: 'shippo',
          logo: 'https://assets-global.website-files.com/6462967bbf70fa5b5b227351/646bd3ac70ee08fca9869afe_shippo-logo-dark.svg',
          status: 'Download'
        },
        {
          id: 4,
          apptitle: 'Loyverse',
          logo: 'https://loyverse.com/sites/all/themes/loyversecom/logo.svg',
          status: 'installed'
        },
        {
          id: 5,
          apptitle: 'storyChief',
          logo: 'https://assets-global.website-files.com/62d66b587db794f6131223e0/62d679136a81955d33635572_logo.svg',
          status: 'download'
        },
        {
          id: 6,
          apptitle: 'Kanban Tools',
          logo: 'https://is1-ssl.mzstatic.com/image/thumb/Purple116/v4/03/2a/24/032a241c-50ad-8fde-bfa4-cd5031e85b23/AppIcon-0-0-1x_U007emarketing-0-0-0-10-0-0-sRGB-0-0-0-GLES2_U002c0-512MB-85-220-0-0.png/1200x630wa.png',
          status: 'installed'
        },
        {
          id: 7,
          apptitle: 'Netlify',
          logo: 'https://cdn.sanity.io/images/o0o2tn5x/production/b7112574694a0fd30064faaa252ad555777cb439-1200x676.png?',
          status: 'download'
        },
        {
          id: 8,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'installed'
        },
        {
          id: 9,
          apptitle: 'Mailchimp',
          logo: 'https://assets.stickpng.com/thumbs/58417f77a6515b1e0ad75a2c.png',
          status: 'Download'
        },
        {
          id: 10,
          apptitle: 'Etsy',
          logo: 'https://1000logos.net/wp-content/uploads/2017/12/Etsy-emblem.jpg',
          status: 'installed'
        },
        {
          id: 11,
          apptitle: 'Basin',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 12,
          apptitle: 'Aweber',
          logo: 'https://www.simplesat.io/wp-content/uploads/2021/12/aweber.png',
          status: 'installed'
        },
        {
          id: 13,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 14,
          apptitle: 'Amazon SQS',
          logo: 'https://miro.medium.com/v2/resize:fit:360/1*qoA4HkaQTAAWHb_tMTi0UA.png',
          status: 'Download'
        },
        {
          id: 15,
          apptitle: 'Basecamp',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 16,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 17,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 18,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 19,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 20,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 21,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 22,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 23,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 24,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        },
        {
          id: 25,
          apptitle: 'Zoom',
          logo: 'https://st2.zoom.us/static/6.3.16094/image/new/topNav/Zoom_logo.svg',
          status: 'Download'
        }
      ],
      filter: 'Download',
      title: 'All Applications',
      isLoading: true,
      search: '',
      value: '',
      idTracker: '',
      timeout: null,
      input: '',
      debouncedInput: '',
      isSearching: false
    }
  },
  computed: {},
  methods: {},
  mounted() {},
  watch: {}
}
</script>

<style scoped>
.container {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.innercontainer {
  width: 87%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.popup {
  width: 40.0625vw;
  height: 40.98360655737705vh;
  box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px, rgba(60, 64, 67, 0.15) 0px 2px 6px 2px;
  border-radius: 0.8rem;
  display: flex;

  flex-direction: column;
  padding: 4px 12px 2px;
}

.innercont {
  width: 98%;
  height: 100%;
  padding: 5px 5px;
  /*  background-color: red; */
}

.header {
  width: 100%;
  font-family: sans-serif;
  font-weight: 700;
  font-size: 18px;
  border-bottom: 1px solid lightgray;
}

.first__row {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 16px;
  /* background-color: green; */
}

.fullrow {
  width: 100%;
}

.full__cont {
  width: 100%;
}

.fullinput__holder {
  width: 100%;
  margin-top: 7px;
}

.fullinput__holder input {
  min-width: 95%;

  /*  border-radius: 0.6rem; */
  outline: none;
  margin: 0;
  font-variant: tabular-nums;
  list-style: none;
  font-feature-settings: 'tnum', 'tnum';
  position: relative;
  display: inline-block;

  padding: 8px 11px;
  color: rgba(0, 0, 0, 0.85);
  font-size: 14px;
  line-height: 1.5715;
  background-color: #fff;
  background-image: none;
  border: 1px solid #d9d9d9;
  border-radius: 8px;
  transition: all 0.3s;
}

.left__cont {
  width: 49%;
  /* s */
}

.label {
  font-size: 18px;
  font-weight: 700;
  line-height: 25px;
}

.right__cont {
  width: 49%;
  /*  background: blue; */
}

.input__holder {
  width: 100%;
  margin-top: 7px;
}

.input__holder input {
  min-width: 90%;
  padding: 14px;

  outline: none;
  margin: 0;
  font-variant: tabular-nums;
  list-style: none;
  font-feature-settings: 'tnum', 'tnum';
  position: relative;
  display: inline-block;

  padding: 8px 11px;
  color: rgba(0, 0, 0, 0.85);
  font-size: 14px;
  line-height: 1.5715;
  background-color: #fff;
  background-image: none;
  border: 1px solid #d9d9d9;
  border-radius: 8px;
  transition: all 0.3s;
}

input:hover {
  border: 1px solid #007fff;
  border-color: 1px solid #007fff;
}

input[type='text']:focus {
  border: 1px solid #007fff;
}

.apikey__cont {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-left: 10px;
  padding-right: 10px;
}

.copy {
  margin-right: 14px;
}

.attention {
  font-size: 24px;
  font-weight: 700;
  color: #007fff;
}
</style>