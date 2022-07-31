<template>
<q-page class="constrain q-pa-md">
  <div class="row q-col-gutter-lg">
    <div class="col-12 col-sm-8">
    <q-card 
      v-for="post in posts"
      :key="post.id"
      class="card-post q-mb-md" 
      flat 
      bordered
      >
      <q-item>
        <q-item-section avatar>
          <q-avatar>
            <img src="https://scontent-iad3-1.xx.fbcdn.net/v/t39.30808-6/240666050_4649097398488481_8002917294674751060_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=09cbfe&_nc_ohc=9I-NJ7mWVRMAX9ch_q7&tn=NIIxpQ274nmieKSR&_nc_ht=scontent-iad3-1.xx&oh=00_AT-U2RK3uca-bVNh6K_fC9Kikst8fd0sylwNw_GGEji2Hw&oe=62EC037B">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-bold">Quamir</q-item-label>
          <q-item-label caption>
            {{post.location}}
          </q-item-label>
        </q-item-section>
      </q-item>
      <q-separator/>
        <q-img :src="post.imageUrl"/>
        <q-card-section>
          <div>{{post.caption}}</div>
          <div class="text-caption text-grey">{{post.date | niceDate}}</div>
        </q-card-section>
      </q-card>
    </div>
    <div class="col-4 large-screen-only">
      <q-item class="fixed">
        <q-item-section avatar>
          <q-avatar size="48px">
            <img src="https://scontent-iad3-1.xx.fbcdn.net/v/t39.30808-6/240666050_4649097398488481_8002917294674751060_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=09cbfe&_nc_ohc=9I-NJ7mWVRMAX9ch_q7&tn=NIIxpQ274nmieKSR&_nc_ht=scontent-iad3-1.xx&oh=00_AT-U2RK3uca-bVNh6K_fC9Kikst8fd0sylwNw_GGEji2Hw&oe=62EC037B">
          </q-avatar>
        </q-item-section>
        <q-item-section>
          <q-item-label class="text-bold">Quamir</q-item-label>
          <q-item-label caption>
            Quamir
          </q-item-label>
        </q-item-section>
      </q-item>
    </div>
  </div>
</q-page>
</template>

<script>
import { date } from 'quasar';
export default {
  name: 'PageHome',
  data(){
    return{
      posts: [
        {
          id: 1,
          caption: 'Fang',
          date: 1659264555149,
          location: 'Richmond, United States',
          imageUrl: 'https://scontent-iad3-1.xx.fbcdn.net/v/t39.30808-6/282560435_5348897808508433_1888507257501302857_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=e3f864&_nc_ohc=_Bs313OjgTUAX_AU5yR&_nc_ht=scontent-iad3-1.xx&oh=00_AT8dY-z1GToFyNY_EEE1FkdvjxnEplr0RP6kephdYjzbFQ&oe=62EAC787'
        },
         {
          id: 2,
          caption: 'Fang',
          date: 1659264555149,
          location: 'Richmond, United States',
          imageUrl: 'https://scontent-iad3-1.xx.fbcdn.net/v/t39.30808-6/282560435_5348897808508433_1888507257501302857_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=e3f864&_nc_ohc=_Bs313OjgTUAX_AU5yR&_nc_ht=scontent-iad3-1.xx&oh=00_AT8dY-z1GToFyNY_EEE1FkdvjxnEplr0RP6kephdYjzbFQ&oe=62EAC787'
        },
         {
          id: 3,
          caption: 'Fang',
          date: 1659264555149,
          location: 'Richmond, United States',
          imageUrl: 'https://scontent-iad3-1.xx.fbcdn.net/v/t39.30808-6/282560435_5348897808508433_1888507257501302857_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=e3f864&_nc_ohc=_Bs313OjgTUAX_AU5yR&_nc_ht=scontent-iad3-1.xx&oh=00_AT8dY-z1GToFyNY_EEE1FkdvjxnEplr0RP6kephdYjzbFQ&oe=62EAC787'
        },
         {
          id: 4,
          caption: 'Fang',
          date: 1659264555149,
          location: 'Richmond, United States',
          imageUrl: 'https://scontent-iad3-1.xx.fbcdn.net/v/t39.30808-6/282560435_5348897808508433_1888507257501302857_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=e3f864&_nc_ohc=_Bs313OjgTUAX_AU5yR&_nc_ht=scontent-iad3-1.xx&oh=00_AT8dY-z1GToFyNY_EEE1FkdvjxnEplr0RP6kephdYjzbFQ&oe=62EAC787'
        },
      ]
    }
  },
  filters:{
    niceDate(value){
      return date.formatDate(value, 'MMMM D h:mmA');
    }
  }
}
</script>

<style lang="scss" scoped>
  .card-post{
    .q-img{
      height: 500px;
      min-height: 200px;

      @media(max-width:  $breakpoint-xs-max){
        height: 300px;
      }
    }
  }
</style>