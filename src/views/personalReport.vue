<template>
  <div>
    <div id="personalContainer"></div>
  </div>
</template>

<script>
import Grid from 'tui-grid';
import {personalReportData} from '../data/basic-dummy.js';

export default {
  name: 'TuiGridComponent',
  mounted(){
    const grid = new Grid({
      el: document.getElementById('personalContainer'),
      data:personalReportData,
      scrollX: false,
      scrollY: false,
      header: {
        height: 50,
        complexColumns: [
        {
            header: '구분',
            name: 'mergeColumn0',
            childNames: ['division', 'device', 'development']
          },
          {
            header: '2022 1Q',
            name: 'mergeColumn1',
            childNames: ['jan', 'feb', 'mar']
          },
          {
            header: '2022 2Q',
            name: 'mergeColumn2',
            childNames: ['apr', 'may', 'jun']
          },
          {
            header: '2022 3Q',
            name: 'mergeColumn3',
            childNames: ['jul', 'aug', 'sep']
          },
          {
            header: '2022 4Q',
            name: 'mergeColumn4',
            childNames: ['oct', 'nov', 'dec']
          },
          {
            header: 'TOTAL',
            name: 'TOTAL',
            childNames: ['Q1', 'Q2', 'Q3', 'Q4']
          },
        ]
      },
      columns: [
        {
          header: 'IP',
          align:'center',
          name: 'ip'
        },
        {
          header: '구분',
          align:'center',
          name: 'division'
        },
        {
          header: '기기',
          align:'center',
          name: 'device'
        },
        {
          header: '개발',
          align:'center',
          name: 'development'
        },
        {
          header: '1월',
          align:'center',
          name: 'jan'
        },
        {
          header: '2월',
          align:'center',
          name: 'feb'
        },
        {
          header: '3월',
          align:'center',
          name: 'mar'
        },
        {
          header: '4월',
          align:'center',
          name: 'apr'
        },
        {
          header: '5월',
          align:'center',
          name: 'may'
        },
        {
          header: '6월',
          align:'center',
          name: 'jun'
        },
        {
          header: '7월',
          align:'center',
          name: 'jul'
        },
        {
          header: '8월',
          align:'center',
          name: 'aug'
        },
        {
          header: '9월',
          align:'center',
          name: 'sep'
        },
        {
          header: '10월',
          align:'center',
          name: 'oct'
        },
        {
          header: '11월',
          align:'center',
          name: 'nov'
        },
        {
          header: '12월',
          align:'center',
          name: 'dec'
        },
        {
          header: '1Q',
          align:'center',
          name: 'Q1'
        },
        {
          header: '2Q',
          align:'center',
          name: 'Q2'
        },
        {
          header: '3Q',
          align:'center',
          name: 'Q3'
        },
        {
          header: '4Q',
          align:'center',
          name: 'Q4'
        },
        {
          header: '2022Total',
          align:'center',
          name: 'total2022'
        },
      ],
      summary: {
        height: 40,
        position: 'bottom', 
        columnContent: {
          jan: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          feb: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          mar: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          apr: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          may: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          jun: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          jul: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          aug: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          sep: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          oct: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          nov: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          dec: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          Q1: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          Q2: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          Q3: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          Q4: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
          total2022: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
        }
    }
  })
}}


</script>

<style scoped>
#gridContainer {
  width: 100%;
  height: 300px;
}
</style>