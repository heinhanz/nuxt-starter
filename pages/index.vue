<script setup>
import { ref } from 'vue';

const showForm = ref(false);
const formSubmitted = ref(false); // Track form submission state

// Function to toggle form visibility
const toggleForm = () => {
  showForm.value = !showForm.value;
};

// Handle form submission
const handleFormSubmit = (event) => {
  event.preventDefault();
  formSubmitted.value = true;

  // Form will be handled by Netlify, wait for success message to show
  setTimeout(() => {
    formSubmitted.value = false; // Reset after 3 seconds
    toggleForm(); // Optionally close the form
  }, 3000);
};
</script>

<template>
  <div class="page-container">
    <div class="content">
      <!-- Logo Container: Replace text with larger, centered logo -->
      <div class="logo-container">
<svg id="Layer_1" style="margin: 10px auto 40px auto;" data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1953.31 774.83">
  <defs>
    <style>
      .cls-1 {
        fill: #fff;
      }

      .cls-1, .cls-2 {
        stroke-width: 0px;
      }

      .cls-2 {
        fill: #ffcd05;
      }
    </style>
  </defs>
  <g>
    <g id="s">
      <g id="c">
        <path id="t" class="cls-2" d="M53.36,336.66l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
        <path id="t-2" data-name="t" class="cls-2" d="M53.36,336.66l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
      </g>
      <g id="a">
        <g id="c-2" data-name="c">
          <path id="t-3" data-name="t" class="cls-2" d="M106.73,375.43h-56.11v28.06l56.11-28.06Z"/>
          <path id="t-4" data-name="t" class="cls-2" d="M106.73,375.43l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
        </g>
        <g id="c-3" data-name="c">
          <path id="t-5" data-name="t" class="cls-2" d="M86.35,438.17l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
          <path id="t-6" data-name="t" class="cls-2" d="M86.35,438.17l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
        </g>
      </g>
      <g id="a-2" data-name="a">
        <g id="c-4" data-name="c">
          <path id="t-7" data-name="t" class="cls-2" d="M0,375.43h56.11v28.06L0,375.43Z"/>
          <path id="t-8" data-name="t" class="cls-2" d="M0,375.43l45.39,32.98,16.49-22.7L0,375.43Z"/>
        </g>
        <g id="c-5" data-name="c">
          <path id="t-9" data-name="t" class="cls-2" d="M20.38,438.17l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
          <path id="t-10" data-name="t" class="cls-2" d="M20.38,438.17l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
        </g>
      </g>
    </g>
    <g id="s-2" data-name="s">
      <g id="c-6" data-name="c">
        <path id="t-11" data-name="t" class="cls-2" d="M1899.95,336.66l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
        <path id="t-12" data-name="t" class="cls-2" d="M1899.95,336.66l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
      </g>
      <g id="a-3" data-name="a">
        <g id="c-7" data-name="c">
          <path id="t-13" data-name="t" class="cls-2" d="M1846.58,375.43h56.11v28.06l-56.11-28.06Z"/>
          <path id="t-14" data-name="t" class="cls-2" d="M1846.58,375.43l45.39,32.98,16.49-22.7-61.88-10.28Z"/>
        </g>
        <g id="c-8" data-name="c">
          <path id="t-15" data-name="t" class="cls-2" d="M1866.97,438.17l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
          <path id="t-16" data-name="t" class="cls-2" d="M1866.97,438.17l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
        </g>
      </g>
      <g id="a-4" data-name="a">
        <g id="c-9" data-name="c">
          <path id="t-17" data-name="t" class="cls-2" d="M1953.31,375.43h-56.11v28.06l56.11-28.06Z"/>
          <path id="t-18" data-name="t" class="cls-2" d="M1953.31,375.43l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
        </g>
        <g id="c-10" data-name="c">
          <path id="t-19" data-name="t" class="cls-2" d="M1932.93,438.17l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
          <path id="t-20" data-name="t" class="cls-2" d="M1932.93,438.17l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
        </g>
      </g>
    </g>
  </g>
  <g>
    <g id="s-3" data-name="s">
      <g id="c-11" data-name="c">
        <path id="t-21" data-name="t" class="cls-2" d="M976.66,0l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
        <path id="t-22" data-name="t" class="cls-2" d="M976.66,0l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
      </g>
      <g id="a-5" data-name="a">
        <g id="c-12" data-name="c">
          <path id="t-23" data-name="t" class="cls-2" d="M1030.02,38.77h-56.11v28.06l56.11-28.06Z"/>
          <path id="t-24" data-name="t" class="cls-2" d="M1030.02,38.77l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
        </g>
        <g id="c-13" data-name="c">
          <path id="t-25" data-name="t" class="cls-2" d="M1009.64,101.5l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
          <path id="t-26" data-name="t" class="cls-2" d="M1009.64,101.5l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
        </g>
      </g>
      <g id="a-6" data-name="a">
        <g id="c-14" data-name="c">
          <path id="t-27" data-name="t" class="cls-2" d="M923.29,38.77h56.11v28.06l-56.11-28.06Z"/>
          <path id="t-28" data-name="t" class="cls-2" d="M923.29,38.77l45.39,32.98,16.49-22.7-61.88-10.28Z"/>
        </g>
        <g id="c-15" data-name="c">
          <path id="t-29" data-name="t" class="cls-2" d="M943.67,101.5l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
          <path id="t-30" data-name="t" class="cls-2" d="M943.67,101.5l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
        </g>
      </g>
    </g>
    <g id="s-4" data-name="s">
      <g id="c-16" data-name="c">
        <path id="t-31" data-name="t" class="cls-2" d="M775.34,146.61l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
        <path id="t-32" data-name="t" class="cls-2" d="M775.34,146.61l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
      </g>
      <g id="a-7" data-name="a">
        <g id="c-17" data-name="c">
          <path id="t-33" data-name="t" class="cls-2" d="M754.96,83.88l45.39,32.98,16.49-22.7-61.88-10.28Z"/>
          <path id="t-34" data-name="t" class="cls-2" d="M754.96,83.88h56.11v28.06s-56.11-28.06-56.11-28.06Z"/>
        </g>
        <g id="c-18" data-name="c">
          <path id="t-35" data-name="t" class="cls-2" d="M808.32,45.1l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
          <path id="t-36" data-name="t" class="cls-2" d="M808.32,45.1l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
        </g>
      </g>
      <g id="a-8" data-name="a">
        <g id="c-19" data-name="c">
          <path id="t-37" data-name="t" class="cls-2" d="M841.3,146.61l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
          <path id="t-38" data-name="t" class="cls-2" d="M841.3,146.61l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
        </g>
        <g id="c-20" data-name="c">
          <path id="t-39" data-name="t" class="cls-2" d="M861.69,83.88l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
          <path id="t-40" data-name="t" class="cls-2" d="M861.69,83.88h-56.11s0,28.06,0,28.06l56.11-28.06Z"/>
        </g>
      </g>
    </g>
    <g id="s-5" data-name="s">
      <g id="c-21" data-name="c">
        <path id="t-41" data-name="t" class="cls-2" d="M718.08,269.84l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
        <path id="t-42" data-name="t" class="cls-2" d="M718.08,269.84l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
      </g>
      <g id="a-9" data-name="a">
        <g id="c-22" data-name="c">
          <path id="t-43" data-name="t" class="cls-2" d="M652.12,269.84l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
          <path id="t-44" data-name="t" class="cls-2" d="M652.12,269.84l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
        </g>
        <g id="c-23" data-name="c">
          <path id="t-45" data-name="t" class="cls-2" d="M631.73,207.1l45.39,32.98,16.49-22.7-61.88-10.28Z"/>
          <path id="t-46" data-name="t" class="cls-2" d="M631.73,207.1h56.11s0,28.06,0,28.06l-56.11-28.06Z"/>
        </g>
      </g>
      <g id="a-10" data-name="a">
        <g id="c-24" data-name="c">
          <path id="t-47" data-name="t" class="cls-2" d="M738.46,207.1l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
          <path id="t-48" data-name="t" class="cls-2" d="M738.46,207.1h-56.11v28.06s56.11-28.06,56.11-28.06Z"/>
        </g>
        <g id="c-25" data-name="c">
          <path id="t-49" data-name="t" class="cls-2" d="M685.1,168.33l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
          <path id="t-50" data-name="t" class="cls-2" d="M685.1,168.33l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
        </g>
      </g>
    </g>
    <g id="s-6" data-name="s">
      <g id="c-26" data-name="c">
        <path id="t-51" data-name="t" class="cls-2" d="M1177.97,146.61l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
        <path id="t-52" data-name="t" class="cls-2" d="M1177.97,146.61l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
      </g>
      <g id="a-11" data-name="a">
        <g id="c-27" data-name="c">
          <path id="t-53" data-name="t" class="cls-2" d="M1198.35,83.88l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
          <path id="t-54" data-name="t" class="cls-2" d="M1198.35,83.88h-56.11v28.06s56.11-28.06,56.11-28.06Z"/>
        </g>
        <g id="c-28" data-name="c">
          <path id="t-55" data-name="t" class="cls-2" d="M1144.99,45.1l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
          <path id="t-56" data-name="t" class="cls-2" d="M1144.99,45.1l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
        </g>
      </g>
      <g id="a-12" data-name="a">
        <g id="c-29" data-name="c">
          <path id="t-57" data-name="t" class="cls-2" d="M1112.01,146.61l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
          <path id="t-58" data-name="t" class="cls-2" d="M1112.01,146.61l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
        </g>
        <g id="c-30" data-name="c">
          <path id="t-59" data-name="t" class="cls-2" d="M1091.62,83.88l45.39,32.98,16.49-22.7-61.88-10.28Z"/>
          <path id="t-60" data-name="t" class="cls-2" d="M1091.62,83.88h56.11s0,28.06,0,28.06l-56.11-28.06Z"/>
        </g>
      </g>
    </g>
    <g id="s-7" data-name="s">
      <g id="c-31" data-name="c">
        <path id="t-61" data-name="t" class="cls-2" d="M1235.23,269.84l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
        <path id="t-62" data-name="t" class="cls-2" d="M1235.23,269.84l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
      </g>
      <g id="a-13" data-name="a">
        <g id="c-32" data-name="c">
          <path id="t-63" data-name="t" class="cls-2" d="M1301.19,269.84l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
          <path id="t-64" data-name="t" class="cls-2" d="M1301.19,269.84l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
        </g>
        <g id="c-33" data-name="c">
          <path id="t-65" data-name="t" class="cls-2" d="M1321.58,207.1l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
          <path id="t-66" data-name="t" class="cls-2" d="M1321.58,207.1h-56.11s0,28.06,0,28.06l56.11-28.06Z"/>
        </g>
      </g>
      <g id="a-14" data-name="a">
        <g id="c-34" data-name="c">
          <path id="t-67" data-name="t" class="cls-2" d="M1214.85,207.1l45.39,32.98,16.49-22.7-61.88-10.28Z"/>
          <path id="t-68" data-name="t" class="cls-2" d="M1214.85,207.1h56.11v28.06s-56.11-28.06-56.11-28.06Z"/>
        </g>
        <g id="c-35" data-name="c">
          <path id="t-69" data-name="t" class="cls-2" d="M1268.21,168.33l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
          <path id="t-70" data-name="t" class="cls-2" d="M1268.21,168.33l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
        </g>
      </g>
    </g>
  </g>
  <g>
    <g id="s-8" data-name="s">
      <g id="c-36" data-name="c">
        <path id="t-71" data-name="t" class="cls-2" d="M976.66,673.33l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
        <path id="t-72" data-name="t" class="cls-2" d="M976.66,673.33l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
      </g>
      <g id="a-15" data-name="a">
        <g id="c-37" data-name="c">
          <path id="t-73" data-name="t" class="cls-2" d="M1030.02,712.1h-56.11v28.06l56.11-28.06Z"/>
          <path id="t-74" data-name="t" class="cls-2" d="M1030.02,712.1l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
        </g>
        <g id="c-38" data-name="c">
          <path id="t-75" data-name="t" class="cls-2" d="M1009.64,774.83l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
          <path id="t-76" data-name="t" class="cls-2" d="M1009.64,774.83l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
        </g>
      </g>
      <g id="a-16" data-name="a">
        <g id="c-39" data-name="c">
          <path id="t-77" data-name="t" class="cls-2" d="M923.29,712.1h56.11v28.06l-56.11-28.06Z"/>
          <path id="t-78" data-name="t" class="cls-2" d="M923.29,712.1l45.39,32.98,16.49-22.7-61.88-10.28Z"/>
        </g>
        <g id="c-40" data-name="c">
          <path id="t-79" data-name="t" class="cls-2" d="M943.67,774.83l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
          <path id="t-80" data-name="t" class="cls-2" d="M943.67,774.83l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
        </g>
      </g>
    </g>
    <g id="s-9" data-name="s">
      <g id="c-41" data-name="c">
        <path id="t-81" data-name="t" class="cls-2" d="M738.46,543.77h-56.11v28.06l56.11-28.06Z"/>
        <path id="t-82" data-name="t" class="cls-2" d="M738.46,543.77l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
      </g>
      <g id="a-17" data-name="a">
        <g id="c-42" data-name="c">
          <path id="t-83" data-name="t" class="cls-2" d="M718.08,606.5l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
          <path id="t-84" data-name="t" class="cls-2" d="M718.08,606.5l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
        </g>
        <g id="c-43" data-name="c">
          <path id="t-85" data-name="t" class="cls-2" d="M652.12,606.5l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
          <path id="t-86" data-name="t" class="cls-2" d="M652.12,606.5l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
        </g>
      </g>
      <g id="a-18" data-name="a">
        <g id="c-44" data-name="c">
          <path id="t-87" data-name="t" class="cls-2" d="M685.1,504.99l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
          <path id="t-88" data-name="t" class="cls-2" d="M685.1,504.99l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
        </g>
        <g id="c-45" data-name="c">
          <path id="t-89" data-name="t" class="cls-2" d="M631.73,543.77h56.11s0,28.06,0,28.06l-56.11-28.06Z"/>
          <path id="t-90" data-name="t" class="cls-2" d="M631.73,543.77l45.39,32.98,16.49-22.7-61.88-10.28Z"/>
        </g>
      </g>
    </g>
    <g id="s-10" data-name="s">
      <g id="c-46" data-name="c">
        <path id="t-91" data-name="t" class="cls-2" d="M861.69,666.99h-56.11s0,28.06,0,28.06l56.11-28.06Z"/>
        <path id="t-92" data-name="t" class="cls-2" d="M861.69,666.99l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
      </g>
      <g id="a-19" data-name="a">
        <g id="c-47" data-name="c">
          <path id="t-93" data-name="t" class="cls-2" d="M841.3,729.73l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
          <path id="t-94" data-name="t" class="cls-2" d="M841.3,729.73l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
        </g>
        <g id="c-48" data-name="c">
          <path id="t-95" data-name="t" class="cls-2" d="M775.34,729.73l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
          <path id="t-96" data-name="t" class="cls-2" d="M775.34,729.73l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
        </g>
      </g>
      <g id="a-20" data-name="a">
        <g id="c-49" data-name="c">
          <path id="t-97" data-name="t" class="cls-2" d="M808.32,628.22l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
          <path id="t-98" data-name="t" class="cls-2" d="M808.32,628.22l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
        </g>
        <g id="c-50" data-name="c">
          <path id="t-99" data-name="t" class="cls-2" d="M754.96,666.99h56.11s0,28.06,0,28.06l-56.11-28.06Z"/>
          <path id="t-100" data-name="t" class="cls-2" d="M754.96,666.99l45.39,32.98,16.49-22.7-61.88-10.28Z"/>
        </g>
      </g>
    </g>
    <g id="s-11" data-name="s">
      <g id="c-51" data-name="c">
        <path id="t-101" data-name="t" class="cls-2" d="M1214.85,543.77h56.11v28.06l-56.11-28.06Z"/>
        <path id="t-102" data-name="t" class="cls-2" d="M1214.85,543.77l45.39,32.98,16.49-22.7-61.88-10.28Z"/>
      </g>
      <g id="a-21" data-name="a">
        <g id="c-52" data-name="c">
          <path id="t-103" data-name="t" class="cls-2" d="M1235.23,606.5l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
          <path id="t-104" data-name="t" class="cls-2" d="M1235.23,606.5l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
        </g>
        <g id="c-53" data-name="c">
          <path id="t-105" data-name="t" class="cls-2" d="M1301.19,606.5l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
          <path id="t-106" data-name="t" class="cls-2" d="M1301.19,606.5l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
        </g>
      </g>
      <g id="a-22" data-name="a">
        <g id="c-54" data-name="c">
          <path id="t-107" data-name="t" class="cls-2" d="M1268.21,504.99l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
          <path id="t-108" data-name="t" class="cls-2" d="M1268.21,504.99l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
        </g>
        <g id="c-55" data-name="c">
          <path id="t-109" data-name="t" class="cls-2" d="M1321.58,543.77h-56.11s0,28.06,0,28.06l56.11-28.06Z"/>
          <path id="t-110" data-name="t" class="cls-2" d="M1321.58,543.77l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
        </g>
      </g>
    </g>
    <g id="s-12" data-name="s">
      <g id="c-56" data-name="c">
        <path id="t-111" data-name="t" class="cls-2" d="M1091.62,666.99h56.11s0,28.06,0,28.06l-56.11-28.06Z"/>
        <path id="t-112" data-name="t" class="cls-2" d="M1091.62,666.99l45.39,32.98,16.49-22.7-61.88-10.28Z"/>
      </g>
      <g id="a-23" data-name="a">
        <g id="c-57" data-name="c">
          <path id="t-113" data-name="t" class="cls-2" d="M1112.01,729.73l17.34-53.36,26.68,8.67-44.02,44.69Z"/>
          <path id="t-114" data-name="t" class="cls-2" d="M1112.01,729.73l45.39-32.98-16.49-22.7-28.9,55.68Z"/>
        </g>
        <g id="c-58" data-name="c">
          <path id="t-115" data-name="t" class="cls-2" d="M1177.97,729.73l-45.39-32.98,16.49-22.7,28.9,55.68Z"/>
          <path id="t-116" data-name="t" class="cls-2" d="M1177.97,729.73l-17.34-53.36-26.68,8.67,44.02,44.69Z"/>
        </g>
      </g>
      <g id="a-24" data-name="a">
        <g id="c-59" data-name="c">
          <path id="t-117" data-name="t" class="cls-2" d="M1144.99,628.22l-17.34,53.36,26.68,8.67-9.34-62.03Z"/>
          <path id="t-118" data-name="t" class="cls-2" d="M1144.99,628.22l17.34,53.36-26.68,8.67,9.34-62.03Z"/>
        </g>
        <g id="c-60" data-name="c">
          <path id="t-119" data-name="t" class="cls-2" d="M1198.35,666.99h-56.11s0,28.06,0,28.06l56.11-28.06Z"/>
          <path id="t-120" data-name="t" class="cls-2" d="M1198.35,666.99l-45.39,32.98-16.49-22.7,61.88-10.28Z"/>
        </g>
      </g>
    </g>
  </g>
  <g>
    <path class="cls-1" d="M258.02,325.07l-47.45,68.25,47.45,68.25h-34.19l-30.42-43.68-30.29,43.68h-34.19l47.45-68.25-47.45-68.25h34.19l30.29,43.55,30.42-43.55h34.19Z"/>
    <path class="cls-1" d="M431.18,325.07h29.77l-47.71,136.5h-32.63l-19.89-56.68-19.76,56.68h-32.63l-47.71-136.5h29.77l34.19,98.02,21.32-60.84-13-37.18h29.77l13,37.18,21.19,60.84,34.32-98.02Z"/>
    <path class="cls-1" d="M472.65,325.07h104.39v28.08h-76.31v28.08h60.32v24.05h-60.32v28.21h76.31v28.08h-104.39v-136.5Z"/>
    <path class="cls-1" d="M710.42,365.24c0,10.92-4.42,20.8-11.44,28.08,7.02,7.28,11.44,17.16,11.44,28.08,0,28.6-21.45,40.17-40.17,40.17h-76.31v-136.5h76.31c22.23,0,40.17,17.94,40.17,40.17ZM682.34,367.19c0-7.8-6.37-14.04-14.04-14.04h-46.28v28.08h46.28c14.04,0,14.04-10.14,14.04-14.04ZM682.34,419.45c0-7.8-6.37-14.17-14.04-14.17h-46.28v28.21h46.28c11.83,0,14.04-10.27,14.04-14.04Z"/>
    <path class="cls-1" d="M867.85,325.07v136.5h-28.08v-65.91l-23.01,65.91h-38.35l-23.01-65.91v65.91h-28.08v-136.5h33.28l37.05,106.08,37.05-106.08h33.15Z"/>
    <path class="cls-1" d="M959.89,325.07l47.71,136.5h-29.77l-9.88-28.08h-48.75l-9.88,28.08h-29.77l47.71-136.5h32.63ZM960.93,413.34l-17.42-49.79-17.42,49.79h34.84Z"/>
    <path class="cls-1" d="M1122.26,403.85c-3.12,3.12-6.76,5.85-10.66,7.93l21.71,49.79h-30.68l-19.24-44.2h-36.01v44.2h-28.08v-136.5h70.33c25.48,0,46.15,20.67,46.15,46.15,0,12.74-5.2,24.31-13.52,32.63ZM1107.69,369.92c0-9.23-7.54-16.77-16.9-16.77h-43.42v36.14h43.42c3.64,0,7.02-1.17,9.75-3.12,4.29-2.99,7.15-8.06,7.15-13.65v-2.6Z"/>
    <path class="cls-1" d="M1222.61,382.27l55.12,79.3h-34.19l-40.17-57.72-22.62,25.35v32.37h-28.08v-136.5h28.08v61.88c14.56-16.25,40.56-45.37,55.38-61.88h37.7l-51.22,57.2Z"/>
    <path class="cls-1" d="M1294.63,325.07h104.39v28.08h-76.31v28.08h60.32v24.05h-60.32v28.21h76.31v28.08h-104.39v-136.5Z"/>
    <path class="cls-1" d="M1482.35,325.07h42.12v24.05h-42.12v112.45h-28.21v-112.45h-42.12v-24.05h70.33Z"/>
    <path class="cls-1" d="M1565.55,447.53c0,7.67-6.24,14.04-14.04,14.04s-14.04-6.37-14.04-14.04,6.24-14.17,14.04-14.17,14.04,6.37,14.04,14.17Z"/>
    <path class="cls-1" d="M1582.45,325.07h104.39v28.08h-76.31v28.08h60.32v24.05h-60.32v28.21h76.31v28.08h-104.39v-136.5Z"/>
    <path class="cls-1" d="M1796.17,325.07h28.21v74.23c0,34.45-27.95,62.27-62.27,62.27s-62.27-27.82-62.27-62.27v-74.23h28.08v74.23c0,18.85,15.34,34.19,34.19,34.19s34.06-15.34,34.06-34.19v-74.23Z"/>
  </g>
</svg>
      </div>

      <h2 class="tagline">Premium Scripts with Unmatched Control</h2>
      <p>Your one-stop shop for premium, never-before-seen scripts. Offering unmatched control over your projects with flexibility and scalability like never before.</p>
      <p>Stay tuned, new products coming soon!</p>

      <!-- Request Service Button -->
      <button class="request-button" @click="toggleForm">Request Service</button>
    </div>
  </div>

  <!-- Contact Form Modal -->
  <div v-if="showForm" class="form-modal">
    <div class="modal-content">
      <h3>Request a Script</h3>
      <form name="contact" method="POST" data-netlify="true" class="contact-form" @submit="handleFormSubmit">
        <!-- Netlify required hidden field for form processing -->
        <input type="hidden" name="form-name" value="contact" />
        
        <p>
          <label for="name">Name</label>
          <input type="text" id="name" name="name" required />
        </p>
        <p>
          <label for="email">Email</label>
          <input type="email" id="email" name="email" required />
        </p>
        <p>
          <label for="script-type">Script Type</label>
          <input type="text" id="script-type" name="script-type" required placeholder="e.g., eCommerce, CMS, Automation" />
        </p>
        <p>
          <label for="budget">Budget</label>
          <input type="number" id="budget" name="budget" required placeholder="e.g., 500 USD" />
        </p>
        <p>
          <label for="timeframe">Timeframe</label>
          <input type="text" id="timeframe" name="timeframe" required placeholder="e.g., 2 weeks, 1 month" />
        </p>
        <p>
          <label for="message">Additional Details</label>
          <textarea id="message" name="message" placeholder="Explain your requirements in detail" required></textarea>
        </p>
        <p>
          <button type="submit">Send Request</button>
        </p>
      </form>
      <button class="close-button" @click="toggleForm">Close</button>

      <!-- Success Notification -->
      <div v-if="formSubmitted" class="success-notification">
        <p>Thank you! Your request has been submitted successfully. We will get back to you soon.</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=TikTok&display=swap');

.page-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #181818;
  margin: 0;
  overflow: auto;
}

.content {
  text-align: center;
  max-width: 600px;
  padding: 40px;
  background-color: #232323;
  border-radius: 15px;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.2);
  color: #fff;
}

.logo-container svg {
  width: 250px; /* Adjust the logo size */
  height: auto;
  margin-bottom: 20px; /* Add some space below the logo */
}

.tagline {
  font-size: 24px;
  color: #ff6f00;
  margin-bottom: 30px;
}

h2 {
  margin: 0;
}

p {
  font-size: 16px;
  color: #bbb;
  line-height: 1.7;
  margin-bottom: 15px;
}

/* Request Service Button */
.request-button {
  background-color: #00ff00;
  color: #181818;
  border: none;
  padding: 12px 24px;
  font-size: 16px;
  cursor: pointer;
  border-radius: 5px;
  margin-top: 30px;
}

.request-button:hover {
  background-color: #33cc33;
}

/* Modal for the Contact Form */
.form-modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  background-color: #333;
  padding: 40px;
  border-radius: 10px;
  width: 100%;
  max-width: 500px;
  text-align: left;
  color: #fff;
}

.modal-content h3 {
  font-size: 24px;
  margin-bottom: 20px;
}

/* Contact Form Styling */
.contact-form {
  display: flex;
  flex-direction: column;
}

.contact-form p {
  margin-bottom: 20px;
}

.contact-form label {
  font-size: 16px;
  color: #fff;
  margin-bottom: 5px;
  display: block;
}

.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #444;
  border-radius: 5px;
  background-color: #222;
  color: #fff;
  font-size: 14px;
}

.contact-form textarea {
  resize: vertical;
  height: 120px;
}

.contact-form button {
  background-color: #00ff00;
  color: #181818;
  border: none;
  padding: 12px 24px;
  font-size: 16px;
  cursor: pointer;
  border-radius: 5px;
  margin-top: 20px;
}

.contact-form button:hover {
  background-color: #33cc33;
}

/* Close button */
.close-button {
  background-color: #ff6f00;
  color: #fff;
  border: none;
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  border-radius: 5px;
  margin-top: 20px;
}

.close-button:hover {
  background-color: #ff8c00;
}

/* Success Notification */
.success-notification {
  background-color: #4caf50;
  color: white;
  padding: 15px;
  border-radius: 5px;
  margin-top: 20px;
  text-align: center;
  font-size: 16px;
}
</style>
