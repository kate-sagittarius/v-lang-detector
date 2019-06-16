<template>
  <v-footer
    height="auto"
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title class="footer">
        <strong class="subheading">Get connected with us on social networks!</strong>

        <v-spacer></v-spacer>

        <SocialButton icon="fab fa-github" iconLink="https://github.com/kate-sagittarius" />
        <SocialButton icon="fab fa-linkedin" iconLink="https://www.linkedin.com/in/kate-zakhovaiko/" />
        <SocialButton icon="fab fa-facebook" iconLink="https://www.facebook.com/profile.php?id=100008213233447" />
        <SocialButton icon="fab fa-instagram" iconLink="https://www.instagram.com/kate_sagittarius/" />

      </v-card-title>

      <v-card-actions class="footer__credits darken-3 justify-center">
        &copy;2019 <strong class="footer__name"> by Kate Zakhobaiko</strong>
      </v-card-actions>
    </v-card>
  </v-footer>
</template>

<script>
import SocialButton from '@/components/SocialButton';

export default {
  name: 'Footer',

  components: {
    SocialButton
    }
}
</script>

<style>
  .footer {
    background-color: #CEE7E6;
  }
  .footer__credits {
    background-color: #FC7753;
    color: #fefefe;
  }
  .footer__name {
    margin-left: 4px;
  }

</style>
