<template>
  <div class="section group">
    <div class="col span_1_of_4 colOne">
        <input type="text" name="code">
    </div>
    <div class="col span_1_of_4">
        <datepicker :format="customFormatter" language="sv"></datepicker>
    </div>
    <div class="col span_1_of_4">
        <select v-model="selected">
            <option disabled value="">Please select one</option>
            <option>A</option>
            <option>B</option>
            <option>C</option>
        </select>
    </div>
    <div class="col span_1_of_4">
    1 of 4
    </div>
  </div>
</template>

<script>
import Datepicker from 'vuejs-datepicker'
import moment from 'moment'

export default {
  name: 'MainTable',
  components: {
    Datepicker
  },
  methods: {
    customFormatter (date) {
      return moment(date).format('YYYY-MMM-DD')
    }
  }
}
</script>

<style lang="scss" scoped>
/*  SECTIONS  */
.section {
    clear: both;
    padding: 0px;
    margin: 0 auto;
    width: 50%;
    input{
        width: 100%;
    }
}

/*  COLUMN SETUP  */
.col {
    display: block;
    float:left;
    margin: 1% 0 1% .5%;
}
.col:first-child { margin-left: 0; }

/*  GROUPING  */
.group:before,
.group:after { content:""; display:table; }
.group:after { clear:both;}
.group { zoom:1; /* For IE 6/7 */ }

/*  GRID OF FOUR  */
.span_4_of_4 {
  width: 100%;
}
.span_3_of_4 {
  width: 74.87%;
}
.span_2_of_4 {
  width: 49.75%;
}
.span_1_of_4 {
  width: 24.62%;
}

/*  GO FULL WIDTH BELOW 480 PIXELS */
@media only screen and (max-width: 480px) {
  .col {  margin: 1% 0 1% 0%; }
  .span_1_of_4, .span_2_of_4, .span_3_of_4, .span_4_of_4 { width: 100%; }
}

.colOne input {
font-size: 14px;
text-align: center;
padding: 4px 0;
}
select{
font-size: 14px;
padding: 4.5px 0;
width: 100%;
}
</style>
