<template>
  <div class="contact">
    <h1>{{ title }}</h1>
    <div class="content contact">
      <!-- address -->
      <div id="address">
        <h3>{{ subtOne }}</h3>
        <p>
          {{ address }}
          <br />
          {{ city }}
          <br />
          {{ zipCode }}
          <br />
          {{ country }}
          <br />
        </p>
      </div>
      <!-- schedule -->
      <div id="schedule">
        <h3>{{ subtTwo }}</h3>
        <ul>
          <!-- looping through the schedule -->
          <li v-for="(schedule, index) in schedules" :key="index">
            {{ schedule }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      // return data for the page
      title: "Contact",
      subtOne: "Address",
      address: "1385 Woodroffe Avenue",
      city: "Ottawa, Ontario",
      zipCode: "K2G 1V8",
      country: "Canada",
      phone: "613-727-4723",
      subtTwo: "Hours of Operation",
      // schedule array
      schedules: [
        "Monday: 8AM-6PM",
        "Tuesday: 8AM-6PM",
        "Wednesday: 8AM-6PM",
        "Thursday: 8AM-6PM",
        "Friday: 8AM-5PM",
        "Saturday: 10AM-4PM",
        "Sunday: 10AM-2PM"
      ]
    };
  }
};
</script>
<style>
#address {
  text-align: left;
}

.contact {
  justify-content: space-between;
  width: 60%;
  margin-left: 20%;
}

#schedule {
  text-align: left;
}
</style>
