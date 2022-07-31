<template>
  <q-page class="constrain-more q-pa-md">
    <div class="camera-frame q-pa-md">
      <img
        class="full-width full-height"
        src="https://scontent-iad3-1.xx.fbcdn.net/v/t39.30808-6/282560435_5348897808508433_1888507257501302857_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=e3f864&_nc_ohc=_Bs313OjgTUAX_AU5yR&_nc_ht=scontent-iad3-1.xx&oh=00_AT8dY-z1GToFyNY_EEE1FkdvjxnEplr0RP6kephdYjzbFQ&oe=62EAC787"
      />
    </div>
    <div class="text-center q-pa-md">
      <q-btn round color="black" icon="eva-camera" size="lg" />
      <div class="row justify-center q-ma-md">
        <q-input v-model="post.caption" class="col col-sm-6" label="Caption" dense />
      </div>
      <div class="row justify-center q-ma-md">
        <q-input v-model="post.location" class="col col-sm-6" label="location" dense>
          <template v-slot:append>
            <q-btn round dense flat icon="eva-navigation-2-outline"></q-btn>
          </template>
        </q-input>
      </div>
      <div class="row justify-center q-ma-md">
        <q-btn unelevated rounded color="primary" label="post image" />
      </div>
    </div>
  </q-page>
</template>

<script>
import { uid } from 'quasar';
export default {
  name: "PageCamera",
  data(){
    return{
      post:{
        id: uid(),
        caption: '',
        location: '',
        photo: null,
        date: Date.now()
      }
    }
  }
};
</script>

<style lang="scss" scoped>
.camera-frame {
  height: 370px;
  width: 100%;
  border: 2px solid $grey-10;
  border-radius: 10px;
}
</style>
