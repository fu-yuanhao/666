<template>
  <div class="p-8 min-h-screen">
    <h1 class="text-4xl font-bold text-purple-400 mb-8">🎴 卡牌库</h1>
    
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div 
        v-for="card in cards"
        :key="card.id"
        class="p-4 bg-gradient-to-b from-gray-800 to-gray-900 border-2 border-purple-500 rounded-lg hover:shadow-lg hover:shadow-purple-400 transition"
      >
        <h3 class="text-xl font-bold text-purple-300">{{ card.name }}</h3>
        <p class="text-sm text-gray-400 mt-2">{{ card.type }}</p>
        <p class="text-sm text-gray-300 mt-3">{{ card.description }}</p>
        <div class="flex justify-between mt-4 text-yellow-400">
          <span>💎 {{ card.cost }}</span>
          <span>{{ card.attack }}/{{ card.health }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const cards = ref([
  {
    id: '1',
    name: '法术飞弹',
    type: '法术',
    cost: 1,
    attack: 0,
    health: 0,
    description: '对一个敌方目标造成 3 伤害',
  },
  {
    id: '2',
    name: '小火元素',
    type: '随从',
    cost: 2,
    attack: 2,
    health: 2,
    description: '无特殊效果',
  },
  {
    id: '3',
    name: '冰霜新星',
    type: '法术',
    cost: 1,
    attack: 0,
    health: 0,
    description: '将所有敌方随从冻结',
  },
  {
    id: '4',
    name: '冰法师',
    type: '随从',
    cost: 3,
    attack: 2,
    health: 3,
    description: '战吼：将一个敌方随从冻结',
  },
  {
    id: '5',
    name: '火焰箭',
    type: '法术',
    cost: 2,
    attack: 0,
    health: 0,
    description: '对一个敌方随从造成 2 伤害',
  },
  {
    id: '6',
    name: '火焰元素',
    type: '随从',
    cost: 5,
    attack: 5,
    health: 5,
    description: '当你打出法术时，造成 1 伤害',
  },
])
</script>