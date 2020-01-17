<template>
  <v-container fluid>
    <v-row class="justify-center text-center">
      <v-col cols="12">
        <v-avatar size="300" color="grey">
          <v-img
            :src="require('../assets/profile2.png')"
            class="my-3"
            contain
            height="300"/>
        </v-avatar>
      </v-col>
      <v-col cols="12">
        <p :class="isXs ? 'display-1' : 'display-2'" class="font-weight-bold mb-3">Yeonwoo Choi</p>
        <p :class="isXs ? 'title' : 'headline'" class="font-weight-regular cyan--text">Coder</p>
      </v-col>
      <v-col cols="12">
        <p :class="isXs ? 'display-2' : 'display-3'" class="grey--text font-weight-light">"Latte is horse"</p>
      </v-col>
      <v-col cols="12">
        <v-row class="justify-end align-center" v-for="item in information" :key="item.icon">
          <v-col cols="4" lg="6" class="text-end">
            <v-icon :large="!isXs" class="pr-5" color="cyan">{{ item.icon }}</v-icon>
          </v-col>
          <v-col cols="8" lg="6" class="text-start">
            <p :class="isXs ? 'body-1' : 'title'" class="title py-0 my-0">{{ item.text }}</p>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',

  data: () => ({
    information: [
      {
        icon: 'fa fa-calendar-alt',
        text: '7st, June 1996 '
      },
      {
        icon: 'fa fa-phone-alt',
        text: '+82 10-000-0000'
      },
      {
        icon: 'fa fa-school',
        text: 'Korea University'
      },
      {
        icon: 'fab fa-google',
        text: 'chldusdn20@google.com'
      },
      {
        icon: 'fab fa-github',
        text: 'Github',
        link: 'https://github.com/yeonwoochoi'
      },
      {
        icon: 'fa fa-users',
        text: 'Team ourHours'
      }
    ]
  }),

  computed: {
    isXs: function () {
      return this.$vuetify.breakpoint.xs
    }
  }
};
</script>
