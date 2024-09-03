<template>
  <v-layout>
    <v-main class="d-flex flex-column pt-16 ga-16">
      <!-- Hero Section -->
      <v-container class="h-100 d-flex align-center pa-6 position-relative" fluid>
        <v-row align="center">
          <v-col cols="12" md="6">
            <div class="text-h6 font-weight-regular">
              Revolutionizing Pickleball with Precision and Connectivity
            </div>

            <h1 class="text-h4 text-md-h2 font-weight-bold mb-6">
              Welcome to PickleFlow
            </h1>

            <div class="text-body-1 text-medium-emphasis mb-10">
              Step into the future of pickleball with PickleFlow, where seamless organization meets community-driven play. Whether you're a player seeking fair matchups and real-time updates, or a club manager looking to streamline operations, PickleFlow transforms every interaction into an effortless experience. Join us in enhancing the sport you love—on and off the court.
            </div>

            <div class="d-flex ga-4 align-center justify-start flex-wrap">
              <v-btn
                class="text-none"
                color="primary"
                flat
                rounded="lg"
                text="Discover more"
              />
            </div>
          </v-col>

          <v-col class="hidden-sm-and-down" cols="6">
            <div class="me-n12">
              <v-sheet border class="ps-4 py-4" color="surface-light" rounded="s-lg">
                <v-img
                  class="border-s border-t border-b"
                  cover
                  max-height="700"
                  position="left"
                  :rounded="$vuetify.display.smAndDown ? true : 's-lg'"
                  :src="heroImgSrc"
                />
              </v-sheet>
            </div>
          </v-col>
        </v-row>

        <div class="v-bg position-absolute top-0 right-0 left-0 bottom-0">
          <div aria-hidden="true" class="overflow-hidden opacity-20 w-100 h-100" />
        </div>
      </v-container>

    <!-- Feature 1 Section -->
    <v-container class="pa-sm-6 pa-md-12" fluid>
      <v-responsive class="text-center mx-auto" max-width="700">
        <p class="font-weight-medium text-primary">Play Better, Manage Smarter</p>

        <p class="mt-2 text-h5 font-weight-bold text-md-h4">
          Everything You Need to Elevate Your Pickleball Experience
        </p>

        <p class="mt-4 text-body-1 text-medium-emphasis">
          PickleFlow is the ultimate tool for both players and organizers, providing all the features you need to streamline play, organize tournaments, and build a connected pickleball community. Whether you're a 2.0 beginner or a 5.0 expert, PickleFlow has you covered.
        </p>
      </v-responsive>

      <v-row class="mt-8">
        <v-col
          v-for="(item, i) in features1"
          :key="i"
          class="d-flex"
          cols="12"
          md="4"
        >
          <v-responsive
            class="mx-auto"
            max-width="500"
            width="100%"
          >
            <v-list-item
              class="px-0"
              rounded="lg"
              :subtitle="item.subtitle"
            >
              <template #title>
                <p class="text-body-2 font-weight-bold pb-2">
                  <v-icon
                    class="mr-2"
                    color="primary"
                    :icon="item.icon"
                    size="small"
                  />
                  {{ item.title }}
                </p>
              </template>

              <v-chip
                append-icon="mdi-arrow-right"
                class="mt-6"
                color="primary"
                link
                size="small"
                text="Learn more"
              />
            </v-list-item>
          </v-responsive>
        </v-col>
      </v-row>
    </v-container>

   <!-- Feature 2 Section -->
<v-container class="pa-sm-6 pa-md-12" fluid>
  <v-responsive class="text-center mx-auto" max-width="700">
    <p class="font-weight-medium text-primary">All the Tools You Need, in One Place</p>

    <p class="mt-2 text-h5 font-weight-bold text-sm-h4">
      Seamless Setup, Smarter Play
    </p>

    <p class="mt-4 text-body-1 text-medium-emphasis">
      Whether you’re managing a tournament or organizing casual play, PickleFlow provides everything you need to make the experience smooth, fair, and enjoyable for everyone.
    </p>
  </v-responsive>

  <v-img
    class="mt-md-12 mt-sm-6"
    cover
    gradient="to bottom, rgba(var(--v-theme-background), 0) 55%, rgba(var(--v-theme-background), 1)"
    min-height="520"
    position="center"
    rounded="lg"
    :src="feature2Src"
  />

  <v-row class="mt-md-8 mt-sm-4">
    <v-col
      v-for="(item, i) in features2"
      :key="i"
      cols="12"
      md="4"
    >
      <v-list-item
        lines="three"
        rounded="lg"
        :subtitle="item.subtitle"
      >
        <template #prepend>
          <v-avatar color="surface-light" :icon="item.icon" rounded>
            <v-icon color="primary" />
          </v-avatar>
        </template>

        <template #title>
          <span class="text-body-2 font-weight-bold">{{ item.title }}</span>
        </template>
      </v-list-item>
    </v-col>
  </v-row>
</v-container>

      <!-- Stat Section -->
      <v-img
        color="primary"
        cover
        :gradient="`to right, rgba(var(--v-theme-primary), 1), rgba(var(--v-theme-primary), .9)`"
        min-height="500"
        :src="statBgSrc"
      >
        <v-container class="pa-md-12 pa-6 d-flex align-content-center flex-wrap h-100" fluid>
          <div class="flex-1-1">
          <p class="font-weight-medium text-primary mb-2">
            Pickleball Growth
          </p>

          <h1 class="font-weight-bold mb-4 text-h5 text-sm-h4 w-100 w-md-33">
            America's Fastest-Growing Sport
          </h1>

          <p class="text-subtitle-2 opacity-60 mb-10 w-100 w-md-50">
            Pickleball is more than just a game; it's a movement. With over 8.9 million players across the United States and thousands of new courts being built each year, this sport is taking the nation by storm. As pickleball continues to expand, PickleFlow is at the forefront, providing advanced tools that simplify organization, enhance player experiences, and support community growth. Whether it's through seamless tournament management or fair play matchmaking, PickleFlow is driving the sport's evolution, making it accessible and enjoyable for all.
          </p>
        </div>

          <v-row
            dense
            justify="center"
          >
            <v-col
              v-for="(stat, i) in stats"
              :key="i"
              class="d-flex"
              cols="12"
              md="3"
              sm="6"
            >
              <v-divider vertical />

              <v-list-item :subtitle="stat.subtitle">
                <template #title>
                  <div class="text-sm-h4 font-weight-bold pb-2">
                    {{ stat.title }}
                  </div>
                </template>
              </v-list-item>
            </v-col>
          </v-row>
        </v-container>
      </v-img>

      <!-- Contact Section -->
      <v-container
        class="pa-2"
        fluid
      >
        <v-responsive
          v-model="form"
          class="mx-auto my-16 px-4"
          max-width="1000"
        >
        <p class="mt-2 text-h5 font-weight-bold text-sm-h4">
          Interested in a Demo? Let's Connect!
        </p>

        <p class="mt-4 mb-10 text-body-1 text-medium-emphasis">
          Discover how PickleFlow can revolutionize your pickleball experience. Whether you're curious about our features or ready to see them in action, we're here to help. Reach out to learn more or schedule a personalized demo.
        </p>

          <v-row>
            <v-col cols="12" md="7">
              <v-row>
                <v-col
                  cols="12"
                  sm="6"
                >
                  <v-text-field
                    v-model="firstName"
                    color="primary"
                    density="compact"
                    :error-messages="errorMessages"
                    label="First Name"
                    placeholder="John"
                    required
                    :rules="[() => !!firstName || 'This field is required']"
                    variant="outlined"
                  />
                </v-col>
                <v-col
                  cols="12"
                  sm="6"
                >
                  <v-text-field
                    v-model="lastName"
                    color="primary"
                    density="compact"
                    :error-messages="errorMessages"
                    label="Last Name"
                    placeholder="Doe"
                    required
                    :rules="[() => !!lastName || 'This field is required']"
                    variant="outlined"
                  />
                </v-col>
                <v-col
                  cols="12"
                  sm="6"
                >
                  <v-text-field
                    v-model="Role"
                    color="primary"
                    density="compact"
                    :error-messages="errorMessages"
                    label="Role"
                    placeholder="General Manager"
                    required
                    :rules="[() => !!budget || 'This field is required']"
                    variant="outlined"
                  />
                </v-col>

                <v-col
                  cols="12"
                  sm="6"
                >
                  <v-text-field
                    v-model="email"
                    color="primary"
                    density="compact"
                    :error-messages="errorMessages"
                    label="email"
                    required
                    :rules="[() => !!email || 'This field is required']"
                    variant="outlined"
                  />
                </v-col>
              </v-row>

              <v-textarea
                v-model="message"
                class="mt-5"
                color="primary"
                density="compact"
                label="Message"
                variant="outlined"
              />

              <v-btn
                class="text-none"
                color="primary"
                height="50"
                text="Let's talk"
                variant="flat"
                width="100%"
              />

              <p class="mt-4 text-medium-emphasis">By submitting this form, I agree to the privacy policy.</p>
            </v-col>

           
          </v-row>
        </v-responsive>
      </v-container>

      <!-- Footer Section -->
      <v-footer class="pa-0 d-flex flex-column">
        <v-sheet
          class="d-flex flex-column flex-sm-row justify-space-between align-center px-4 py-2 w-full"
          color="surface-light"
          variant="flat"
          width="100%"
        >
          <p class="text-caption">
            &copy; 2016-{{ new Date().getFullYear() }} Vuetify. All rights reserved.
          </p>

          <div>
            <v-btn
              v-for="icon in footerIcons"
              :key="icon"
              :icon="icon"
              size="small"
              variant="text"
            />
          </div>
        </v-sheet>
      </v-footer>
    </v-main>
  </v-layout>
</template>

<script setup>
  import { computed, shallowRef } from 'vue'
  import { useTheme } from 'vuetify'
  // Import the main.scss file for global styles
  import '../assets/main.scss'

  const theme = useTheme()

  // Define Values for Hero Section

  const heroImgSrc = computed(() => `https://cdn.vuetifyjs.com/docs/images/one/snips/screenshots/vuetify-get-started-${theme.current.value.dark ? 'dark' : 'light'}.png`)

  // Define Values for Logo Section

  const logos = computed(() => ([
    {
      href: 'https://bin.vuetifyjs.com/',
      src: `https://vuetifyjs.b-cdn.net/docs/images/one/logos/vbin-logo-${theme.current.value.dark ? 'dark' : 'light'}.png`,
    },
    {
      href: 'https://issues.vuetifyjs.com/',
      src: `https://vuetifyjs.b-cdn.net/docs/images/one/logos/vissues-logo-${theme.current.value.dark ? 'dark' : 'light'}.png`,
    },
    {
      href: 'https://vuetifyjs.com/?one=subscribe',
      src: `https://vuetifyjs.b-cdn.net/docs/images/one/logos/vone-logo-${theme.current.value.dark ? 'dark' : 'light'}.png`,
    },
    {
      href: 'https://play.vuetifyjs.com/',
      src: `https://vuetifyjs.b-cdn.net/docs/images/one/logos/vplay-logo-${theme.current.value.dark ? 'dark' : 'light'}.png`,
    },
    {
      href: 'https://studio.vuetifyjs.com/',
      src: `https://vuetifyjs.b-cdn.net/docs/images/one/logos/vstudio-logo-${theme.current.value.dark ? 'dark' : 'light'}.png`,
    },
  ]))

  // Define Values for Features Section 1

  const features1 = [
    {
      title: 'Seamless Open Play',
      subtitle:
        'Dive into the action with PickleFlow’s Open Play system, which effortlessly organizes games based on skill levels and availability. Whether you’re a beginner or a seasoned player, getting into a match has never been easier.',
      icon: 'mdi-tennis-ball',
    },
    {
      title: 'ELO-Based Scoring',
      subtitle:
        'Enjoy competitive play without the hassle of setting up a DUPR account. PickleFlow’s ELO-based scoring system automatically tracks your progress, making it ideal for beginners and those looking to improve their game.',
      icon: 'mdi-chart-line',
    },
    {
      title: 'Fair Play Matching',
      subtitle:
        'Keep the fun in the game with PickleFlow’s Fair Play system, which ensures that beginners aren’t paired against advanced players. This feature promotes balanced matches, making the experience enjoyable for everyone.',
      icon: 'mdi-scale-balance',
    },
  ]


  const features2 = [
  {
    title: 'On- and Offline Kiosk',
    subtitle:
      'Effortlessly manage player check-ins with PickleFlow’s kiosk system, available both online and offline. Utilize barcode scanning to quickly and efficiently check players in and out, ensuring a smooth experience regardless of internet connectivity.',
    icon: 'mdi-kiosk-outline',
  },
  {
    title: 'AI-Driven Tournament Management',
    subtitle:
      'Streamline your tournaments with AI-driven decisions for formats like ladder, round robin, knockout, and more. PickleFlow’s intelligent system ensures fair play and optimal match scheduling, making every event a success.',
    icon: 'mdi-robot-outline',
  },
  {
    title: 'Fair and Fun Open Play',
    subtitle:
      'Keep the game enjoyable for everyone with PickleFlow’s Fair Play Matching system. This feature balances skill levels and player rotations, ensuring that beginners aren’t paired with advanced players, promoting a fun and inclusive environment.',
    icon: 'mdi-emoticon-happy-outline',
  },
  {
    title: 'Effortless Player Check-Ins',
    subtitle:
      'Simplify your event management with quick barcode scanning for player check-ins. Reduce wait times and keep the event flowing smoothly, whether it’s an open play session or a competitive tournament.',
    icon: 'mdi-barcode-scan',
  },
  {
    title: 'Customizable Play Formats',
    subtitle:
      'Adapt to any event with PickleFlow’s customizable play formats. From casual games to structured tournaments, PickleFlow offers the flexibility to create the perfect pickleball experience.',
    icon: 'mdi-cog-outline',
  },
  {
    title: 'Robust Data Management',
    subtitle:
      'Ensure your player data and match results are secure with reliable database backups and advanced security features. PickleFlow keeps your information safe and easily accessible.',
    icon: 'mdi-database-lock-outline',
  },
];


  const feature2Src = computed(() => `https://cdn.vuetifyjs.com/docs/images/one/snips/screenshots/vuetify-get-started-${theme.current.value.dark ? 'dark' : 'light'}.png`)

 // Define Values for Stat Section

const statBgSrc = computed(() => `https://images.unsplash.com/photo-1521737604893-d14cc237f11d?q=80&w=1484&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D`)

const stats = [
  {
    title: '8.9m+',
    subtitle: 'Pickleball players in the U.S. (2023)',
  },
  {
    title: '10,000+',
    subtitle: 'Pickleball courts nationwide',
  },
  {
    title: '3x',
    subtitle: 'Fastest-growing sport in the U.S. for 3 consecutive years',
  },
  {
    title: '50+',
    subtitle: 'Countries playing pickleball worldwide',
  },
]

  const form = shallowRef(false)
  const errorMessages = shallowRef('')
  const firstName = shallowRef(null)
  const lastName = shallowRef(null)
  const budget = shallowRef(null)
  const website = shallowRef(null)
  const message = shallowRef(null)


  // Define Values for Footer Section

  const footerIcons = [
    'mdi-facebook',
    'mdi-twitter',
    'mdi-linkedin',
    'mdi-instagram',
  ]
</script>

<style>
  .v-bg {
    pointer-events: none;
    filter: blur(56px);
  }

  .v-bg > div {
    background: linear-gradient(
      to bottom right,
      rgb(var(--v-theme-info)),
      rgb(var(--v-theme-primary))
    );
    z-index: -40;
    clip-path: polygon(10% 10%, 20% 10%, 70% 80%, 60% 80%, 30% 5%, 40% 10%, 50% 30%, 60% 50%, 50% 5%, 55% 15%, 45% 15%, 50% 5%, 30% 80%, 40% 85%, 35% 95%, 25% 90%);
  }
</style>
