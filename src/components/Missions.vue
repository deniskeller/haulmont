<template>
  <div class="">
    <div class="missions">
      <MissionItem
        v-for="mission in missions" :key="mission.title"
        :subtitle="mission.subtitle"
        :title="mission.title"
        :image="mission.image"
        :paragraph="mission.paragraph"
        :appointed_date="mission.appointed_date"
        :appointed_time="mission.appointed_time"
        :appointed_rocket="mission.appointed_rocket"
        class="missions__item"/>
    </div>      
  </div>
</template>

<script>
import MissionItem from '../components/MissionItem';
export default {
  name: "Missions",
  components: {
    MissionItem,
  },
  data(){
    return {
      missions: [
        {
          "subtitle": "Mission 1",
          "title": "SAOCOM 1B, GNOMES-1, Tyvak-0172",
          "image": "falcon.svg",
          "paragraph": [
            "SpaceX's Falcon 9 will launch the second of the two satellite SAOCOM 1 satellites into a sun-synchronous polar orbit from SLC-40, Cape Canaveral AFS. SAOCOM 1B is a synthetic aperture radar Earth observation satellite to support disaster management. ",
            "The SAOCOM spacecraft are operated by CONAE, the Argentinian National Space Activities Commission, and are built by INVAP. This mission is also expected to include rideshare payloads Sequoia, and GNOMES-1. This will be the first polar launch from the Space Coast in 60 years. The launch azimuth will be southward and the booster will land at LZ-1.",
            "The SAOCOM spacecraft are operated by CONAE, the Argentinian National Space Activities Commission, and are built by INVAP. This mission is also expected to include rideshare payloads Sequoia, and GNOMES-1. This will be the first polar launch from the Space Coast in 60 years. The launch azimuth will be southward and the booster will land at LZ-1."
          ],
          "appointed_date": "2020-08-30",
          "appointed_time": "23:18:00",
          "appointed_rocket": "Falcon 9"
        },
        {
          "subtitle": "Mission 2",
          "title": "Starlink-12 (v1.0)",
          "image": "starlink.svg",
          "paragraph": [
            "This mission will launch the twelfth batch of operational Starlink satellites, which are expected to be version 1.0, from SLC-40, Cape Canaveral Air Force Station. It is the thirteenth Starlink launch overall. The satellites will be delivered to low Earth orbit and will spend a few weeks maneuvering to their operational altitude of 550 km. The booster for this mission is expected to land on an ASDS"
          ],
          "appointed_date": "2020-10-06",
          "appointed_time": "11:29:00",
          "appointed_rocket": "Falcon 9"
        },
        {
          "subtitle": "Mission 3",
          "title": "Crew-1",
          "image": "crew.svg",
          "paragraph": [
            "SpaceX will launch the first operational mission of its Crew Dragon vehicle as part of NASA's Commercial Crew Transportation Capability Program (CCtCap), carrying 3 NASA astronauts and 1 JAXA astronaut to the International Space Station. This mission will be the second crewed flight to launch from the United States since the end of the Space Shuttle program in 2011"
          ],
          "appointed_date": "2020-11-16",
          "appointed_time": "00:27:00",
          "appointed_rocket": "Falcon 9"
        }
      ]
    }
  }
};
</script>

<style scoped lang="scss">
.missions {
  &__item {
    margin-bottom: em(20px);
  }
  &__item:last-child {
    margin-bottom: 0px;
  }
}

</style>
