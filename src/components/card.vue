<template>
  <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="my-card q-ma-xl" flat bordered>
      <q-img src="https://images.unsplash.com/photo-1438761681033-6461ffad8d80?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1500&q=80" />

      <q-card-section>
        <div class="text-overline text-orange-9">Desarrolladores</div>
        <div class="text-h5 q-mt-sm q-mb-xs">Marisa Avila</div>
        <div class="text-caption text-grey">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua.
        </div>
      </q-card-section>

      <q-card-actions>

        <q-btn
          color="grey"
          round
          flat
          dense
          :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
          @click="expanded = !expanded"
        />
      </q-card-actions>

      <q-slide-transition>
        <div v-show="expanded">
          <q-separator />
          <q-card-section class="text-subitle2">
            <div class="q-pa-md" style="max-width: 500px">
              <q-list bordered>
                 <q-item clickable v-ripple>
                    <q-item-section avatar>
                        <q-icon color="orange-9" name="local_phone" />
                    </q-item-section>

                    <q-item-section>{{ telefono }}</q-item-section>
                 </q-item>

                 <q-item clickable v-ripple>
                    <q-item-section avatar>
                        <q-icon color="orange-9" name="mail" />
                    </q-item-section>

                    <q-item-section> {{ mail }}</q-item-section>
                 </q-item>
              </q-list>
            </div>

          </q-card-section>
        </div>
      </q-slide-transition>
    </q-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      expanded: false,
      telefono: '3794 065345',
      mail: 'marisaavila@gmail.com'
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 350px
</style>
