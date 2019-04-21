<template>
  <div>
    <b-card border-variant="light" header="轉蛋機率計算" class="text-center">
      <b-card-text>
        <b-form @submit="onSubmit" @reset="onReset" v-if="show">
          <b-form-group id="fivestar-group" label="五星PU幾騎:" label-for="fivestar-select">
            <b-form-select
              id="fivestar-select"
              v-model="form.fiveStar"
              :options="fiveStars"
              required
            ></b-form-select>
          </b-form-group>

          <b-form-group id="fourstar-group" label="四星PU幾騎:" label-for="fourstar-select">
            <b-form-select
              id="fourstar-select"
              v-model="form.fourStar"
              :options="fourStars"
              required
            ></b-form-select>
          </b-form-group>
          <b-form-group id="threestar-group" label="三星PU幾騎:" label-for="threestar-select">
            <b-form-select
              id="threestar-select"
              v-model="form.threeStar"
              :options="threeStars"
              required
            ></b-form-select>
          </b-form-group>

          <b-form-group id="input-group-4">
            <b-form-checkbox-group v-model="form.checked" id="checkboxes-4">
              <b-form-checkbox value="me">Check me out</b-form-checkbox>
              <b-form-checkbox value="that">Check that out</b-form-checkbox>
            </b-form-checkbox-group>
          </b-form-group>

          <b-button type="submit" variant="primary">Submit</b-button>
          <b-button type="reset" variant="danger">Reset</b-button>
        </b-form>
        <b-card class="mt-3" header="轉蛋結果">
          <pre class="m-0">五星PU：{{ form.fiveStar}}騎<br>四星PU：{{ form.fourStar}}騎<br>三星PU：{{ form.threeStar}}騎<br>{{form.checked }}<br>{{lastresult }}</pre>
        </b-card>
      </b-card-text>
    </b-card>
  </div>
</template>

<script>
export default {
  name: "Gashapon",
  data() {
    return {
      form: {
        fiveStar: null,
        fourStar: null,
        threeStar: null,
        checked: [],
        result: null
      },
      fiveStars: [
        { text: "請選擇", value: null },
        { text: "一騎", value: 1 },
        { text: "兩騎", value: 2 },
        { text: "三騎", value: 3 },
        { text: "四騎", value: 4 }
      ],
      fourStars: [
        { text: "請選擇", value: null },
        { text: "一騎", value: 1 },
        { text: "兩騎", value: 2 },
        { text: "三騎", value: 3 },
        { text: "四騎", value: 4 }
      ],
      threeStars: [
        { text: "請選擇", value: null },
        { text: "一騎", value: 1 },
        { text: "兩騎", value: 2 },
        { text: "三騎", value: 3 },
        { text: "四騎", value: 4 }
      ],
      show: true
    };
  },
  computed: {
    lastresult: function() {
      return this.form.fiveStar + 1;
    }
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset(evt) {
      evt.preventDefault();
      // Reset our form values
      this.form.fiveStar = null;
      this.form.fourStar = null;
      this.form.threeStar = null;
      this.form.checked = [];
      this.form.result = null;
      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
      });
    }
  }
};
</script>