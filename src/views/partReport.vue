<template>
  <div>
    <div>형태별 제작 수량</div>
    <div id="shapeContainer"></div>

    <br />
    <br />
    <br />
    <br />
    <br />

    <div>인원별 투입내역</div>
    <div id="individualContainer"></div>
  </div>
</template>

<script>
import Grid from 'tui-grid';
import axios from "axios";
let shapeGrid, individualGrid;

export default {
  name: 'TuiGridComponent',
  data(){
    return{
      personalReportData: [],
      individualReportData: [],
    }
  },
  async mounted(){
    shapeGrid = new Grid({
      el: document.getElementById('shapeContainer'),
      data: this.personalReportData,
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
    individualGrid = new Grid({
      el: document.getElementById('individualContainer'),
      data: [
        {
          "divide":"권지현'",
          "Q1":51.5, 
          "Q2":106,
          "Q3":107,
          "Q4":24,
          "total2022":288.5,
          "MM":1.45
        },
        {
          "divide":"진소민",
          "Q1":44, 
          "Q2":59,
          "Q3":110,
          "Q4":3,
          "total2022":216,
        },
        {
          "divide":"장은지",
          "Q1":9, 
          "Q2":45,
          "Q3":39,
          "Q4":0,
          "total2022":93,
          "MM":1.3
        },
        {
          "divide":"최재민",
          "Q1":9, 
          "Q2":45,
          "Q3":39,
          "Q4":0,
          "total2022":93,
          "MM":1.3
        },
      ],
      scrollX: false,
      scrollY: false,
      header: {
        height: 50,
      },
      columns: [
        {
          header: '구분',
          align:'center',
          name: 'divide'
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
          header: '2022 Total',
          align:'center',
          name: 'total2022'
        },
        {
          header: 'M/M',
          align:'center',
          name: 'MM'
        },
      ],
      summary: {
        height: 40,
        position: 'bottom', 
        columnContent: {
          total2022: {
            template: function(valueMap) {
              return `${valueMap.sum}`;
            }
          },
        }
    }
  })

  this.personalReport();
  this.individualReport();
},
methods:{
  async personalReport(){
      await axios.get("https://3a41448b-2501-454a-a51f-810af056121a.mock.pstmn.io/personalReportList")
        .then((response)=>{
          this.personalReportData = response.data;
          shapeGrid.resetData(this.personalReportData);
        })
        .catch((err)=>console.log(err))
    },
  async individualReport(){
    await axios.get("https://3a41448b-2501-454a-a51f-810af056121a.mock.pstmn.io/partReportList")
      .then((response)=>{
        this.individualReportData = response.data;
        individualGrid.resetData(this.individualReportData);
      })
      .catch((err)=>console.log(err))
    }
  }
}


</script>

<style scoped>
#gridContainer {
  width: 100%;
  height: 300px;
}
</style>