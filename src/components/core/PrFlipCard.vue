<template>
    <div class="flip-card">
        <div class="flip-card-inner">
            <div class="flip-card-front" :style="{backgroundImage: `url(${prod.picture})`}">
                <div class="flip-card_protrait">
                    <h3>{{ prod.title }}</h3>
                    <div class="flip-tags">
                        <span v-for="tag in prod.tags" class="flip-tag">{{ tag }}</span>
                    </div>
                </div>
            </div>
            <div class="flip-card-back">
                <h3>{{ prod.title }}</h3>
                <p class="short-description">{{ prod.description }}</p>
                <a :href="prod.link" target="_blank" class="flip-cta">see more</a>
            </div>
        </div>
    </div>
</template>

<script setup>


const {prod} = defineProps(["prod"]);

</script>

<style>
.flip-card {
  background-color: transparent;
  width: 250px;
  height: 300px;
  perspective: 1000px;
  border-radius: 3px;
}

.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
  border-radius: 10px;
  padding: 10px;
}

.flip-card-front {
  background-color: #bbb;
  color: white;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.flip-card-back {
  background-color: blueviolet;
  color: white;
  transform: rotateY(180deg);
  display: flex;
  flex-direction: column;
}

.flip-card-back .short-description {
    flex: 5;
    overflow: hidden;
    text-overflow: ellipsis;
    text-align: left;
    max-height: calc(1rem * 33);

}

.flip-card_protrait {
    background-color: #000a;
    border-radius: 10px;
    height: calc(100% + 20px);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
    margin: -10px;
}
.flip-tag {
    display: inline-block;
    margin: 2px;
    padding: 5px;
    background-color: gray;
    border-radius: 10px;
}

.flip-tags {
    display: flex;
    flex-wrap: wrap;
}

.flip-cta{
    background-color: white;
    border-radius: 10px;
    margin: 5px;
    text-decoration: none;
    color: blueviolet;
}
</style>