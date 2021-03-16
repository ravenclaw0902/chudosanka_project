<template>
  <div class="flex flex-center text-center">
    <q-splitter v-model="splitterModel" style="height: 250px">
      <template v-slot:before>
        <q-tabs v-model="tab" vertical class="text-teal">
          <q-tab v-for="tab in tabs" :key="tab.name" v-bind="tab" />
        </q-tabs>
      </template>

      <template v-slot:after>
        <q-tab-panels
          v-model="tab"
          animated
          swipeable
          vertical
          transition-prev="jump-up"
          transition-next="jump-up"
        >
          <q-tab-panel v-for="tab in tabs" :key="tab.name" v-bind="tab">
            <div class="text-h4 q-mb-md">{{ tab['title'] }}</div>
            <p>{{ tab['caption'] }}</p>
          </q-tab-panel>
        </q-tab-panels>
      </template>
    </q-splitter>
  </div>
</template>

<script>
export default {
  name: 'MainTabMembers',

  data() {
    return {
      tabs: [
        {
          name: 'massage',
          title: 'Массажисты',
          icon: '',
          caption:
            'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.'
        },
        {
          name: 'children',
          title: 'Педиатры',
          icon: '',
          caption:
            'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.'
        },
        {
          name: 'physician',
          title: 'ЛФК',
          icon: '',
          caption:
            'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis praesentium cumque magnam odio iure quidem, quod illum numquam possimus obcaecati commodi minima assumenda consectetur culpa fuga nulla ullam. In, libero.'
        }
      ]
    }
  }
}
</script>