<template>
    <div class="admin">

        <canvas id="myChart"></canvas>

    </div>
</template>


<script>
    import Chart from 'chart.js/dist/Chart.min'


    export default {
        name: 'admin',

        mounted() {

            let ctx = document.getElementById("myChart").getContext('2d');
            let myChart = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ["Posts", "Categories", "Comments"],
                    datasets: [{
                        label: 'Data of CMS',
                        data: ['', '', ''],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
                    borderColor: [
                'rgba(255,99,132,1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
                    borderWidth: 1
        }]
        },
            options: {
                scales: {
                    yAxes: [{
                        ticks: {
                            beginAtZero:true
                        }
                    }]
                }
            }
        });


        }// MOUNTED

    }
</script>


<style>
</style>