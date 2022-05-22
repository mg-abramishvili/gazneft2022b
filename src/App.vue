<template>
    <div class="wrapper">
        <template v-for="(page, index) in pages">
            <div v-if="selected.page == index + 1" class="page">
                <img :src="page" alt="" />

                <div v-if="selected.page == 1" class="index">
                    <div class="col">
                        <h2 style="color: #1D74BB;">Инновации</h2>
                        <ul>
                            <li @click="selectPage(2)">Система удаленного мониторинга <br>газоперекачивающих агрегатов (трендовый контроль)</li>
                            <li @click="selectPage(3)">Блок спектрального анализа</li>
                            <li @click="selectPage(4)">Система обнаружения метана <br>в атмосферном воздухе технологических площадок КС</li>
                            <li @click="selectPage(5)">Камера сгорания <br>ООО НПП «Газтурбомаш» для ГПА типа ГТН-6</li>
                            <li @click="selectPage(6)">Подшипники скольжения с полимерным покрытием</li>
                            <li @click="selectPage(7)">Прототип системы мониторинга и предиктивной аналитики</li>
                            <li @click="selectPage(8)">Схема продувки пылеуловителей <br>без стравливания газа в атмосферу</li>
                            <li @click="selectPage(9)">Портативный лазерный детектор утечек метана</li>
                            <li @click="selectPage(10)">Подогреватель газа ПАО «АК ВНЗМ»</li>
                            <li @click="selectPage(11)">Реализация алгоритмов в САУиР ГРС</li>
                            <li @click="selectPage(12)">Автоматическая регистрация <br>комплексных проверок алгоритмов ГРС и кранов ЛЧ</li>
                            <li @click="selectPage(13)">Программно-технический комплекс «Смарт-мониторинг»</li>
                            <li @click="selectPage(14)">Методика оценки опасности участков газопроводов <br>с радиусами изгибов менее 250Dн</li>
                        </ul>
                    </div>
                    <div class="col">
                        <h2>&nbsp;</h2>
                        <ul>
                            <li @click="selectPage(15)">Способ определения напряженно-деформированных участ-<br>ков газопровода после укладки трубопровода в траншею</li>
                            <li @click="selectPage(16)">Способ вытеснения газовоздушной смеси <br>из отремонтированного участка МГ</li>
                            <li @click="selectPage(17)">Распределитель защитного тока (РЗТ)</li>
                            <li @click="selectPage(18)">Применение сварочных аппаратов нового поколения</li>
                            <li @click="selectPage(19)">Применение комплексов цифровой радиографии нового по-<br>коления</li>
                            <li @click="selectPage(20)">Внедрение современных гамма-дефектоскопов <br>Exertus Dual 120</li>
                            <li @click="selectPage(21)">Опытно-промышленная эксплуатация оборудования АНУВМ</li>
                            <li @click="selectPage(22)">Индуктор НИП-400 <br>для снятия заводского изоляционного покрытия</li>
                            <li @click="selectPage(23)">Устройство для сбора отходов изоляции</li>
                            <li @click="selectPage(24)">Методика автоматического расчета запаса газа в ГТС</li>
                            <li @click="selectPage(25)">Увеличение ресурса узлов машин и механизмов</li>
                            <li @click="selectPage(26)">Подсчет запасов подземных вод</li>
                            <li @click="selectPage(27)">Раздельный сбор отходов</li>
                        </ul>
                    </div>
                    <div class="col">
                        <h2 style="color: #107883;">Компетенции</h2>
                        <ul>
                            <li @click="selectPage(28)">Проект «ГАЗПРОМ-КЛАСС»</li>
                            <li @click="selectPage(29)">Проект «Предуниверсарий»</li>
                            <li @click="selectPage(30)">Образовательные проекты УГНТУ для школьников <br>и студентов Республики Башкортостан</li>
                            <li @click="selectPage(31)">I Слет целевых студентов ПАО «Газпром»</li>
                            <li @click="selectPage(32)">Проект «ГАЗПРОМ-ГРУППА»</li>
                            <li @click="selectPage(33)">Базовые кафедры ООО «Газпром трансгаз Уфа» <br>на базе ФГБОУ ВО «Уфимский государственный нефтяной <br>технический университет»</li>
                            <li @click="selectPage(34)">Базовые кафедры ООО «Газпром трансгаз Уфа» <br>на базе ФГБОУ ВО «Уфимский государственный <br>авиационный технический университет»</li>
                            <li @click="selectPage(35)">Научно-технический полигон</li>
                            <li @click="selectPage(36)">Программа подготовки специалистов по АЛ-31 СТ</li>
                            <li @click="selectPage(37)">ФГБОУ ВО «Уфимский государственный нефтяной <br>технический университет»</li>
                        </ul>
                    </div>
                </div>
            </div>
        </template>
        <div v-if="views.panel" class="panel">
            <button @click="selectPage(1)">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-house" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M2 13.5V7h1v6.5a.5.5 0 0 0 .5.5h9a.5.5 0 0 0 .5-.5V7h1v6.5a1.5 1.5 0 0 1-1.5 1.5h-9A1.5 1.5 0 0 1 2 13.5zm11-11V6l-2-2V2.5a.5.5 0 0 1 .5-.5h1a.5.5 0 0 1 .5.5z"/>
                    <path fill-rule="evenodd" d="M7.293 1.5a1 1 0 0 1 1.414 0l6.647 6.646a.5.5 0 0 1-.708.708L8 2.207 1.354 8.854a.5.5 0 1 1-.708-.708L7.293 1.5z"/>
                </svg>
            </button>
            <button v-if="selected.page == 38" @click="selectPage(37)">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-left-short" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M12 8a.5.5 0 0 1-.5.5H5.707l2.147 2.146a.5.5 0 0 1-.708.708l-3-3a.5.5 0 0 1 0-.708l3-3a.5.5 0 1 1 .708.708L5.707 7.5H11.5a.5.5 0 0 1 .5.5z"/>
                </svg>
            </button>
            <button v-if="selected.page == 37" @click="selectPage(38)">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-right-short" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M4 8a.5.5 0 0 1 .5-.5h5.793L8.146 5.354a.5.5 0 1 1 .708-.708l3 3a.5.5 0 0 1 0 .708l-3 3a.5.5 0 0 1-.708-.708L10.293 8.5H4.5A.5.5 0 0 1 4 8z"/>
                </svg>
            </button>
        </div>

        <div v-if="views.fadeout" class="fadeout"></div>

        <v-idle :duration="60" :events="['click', 'touchstart', 'touchmove', 'touchend', 'mousemove', 'scroll']" @idle="selectPage(1)" />
    </div>
</template>

<script>
export default {
    data() {
        return {
            pages: [
                '/pages/01.png',
                '/pages/02.jpg',
                '/pages/03.jpg',
                '/pages/04.jpg',
                '/pages/05.jpg',
                '/pages/06.jpg',
                '/pages/07.jpg',
                '/pages/08.jpg',
                '/pages/09.jpg',
                '/pages/10.jpg',
                '/pages/11.jpg',
                '/pages/12.jpg',
                '/pages/13.jpg',
                '/pages/14.jpg',
                '/pages/15.jpg',
                '/pages/16.jpg',
                '/pages/17.jpg',
                '/pages/18.jpg',
                '/pages/19.jpg',
                '/pages/20.jpg',
                '/pages/21.jpg',
                '/pages/22.jpg',
                '/pages/23.jpg',
                '/pages/24.jpg',
                '/pages/25.jpg',
                '/pages/26.jpg',
                '/pages/27.jpg',
                '/pages/28.jpg',
                '/pages/29.jpg',
                '/pages/30.jpg',
                '/pages/31.jpg',
                '/pages/32.jpg',
                '/pages/33.jpg',
                '/pages/34.jpg',
                '/pages/35.jpg',
                '/pages/36.jpg',
                '/pages/37.jpg',
                '/pages/38.jpg',
            ],

            selected: {
                page: 1,
            },

            views: {
                panel: false,
                fadeout: false,
            }
        }
    },
    mounted() {
        document.oncontextmenu = new Function("return false;")
    },
    methods: {
        selectPage(page) {
            if(this.selected.page == page) {
                return
            }

            this.views.fadeout = true

            setTimeout(() => {
                this.selected.page = page

                if(this.selected.page == 1) {
                    this.views.panel = false
                } else {
                    this.views.panel = true
                }
            }, 150)

            setTimeout(() => {
                this.views.fadeout = false
            }, 300)
        },
    }
}
</script>

<style>
html, body {
        margin: 0;
        position: relative;
        width: 1920px;
        height: 1080px;
        overflow: hidden;
        font-family: 'HeliosCond';
        font-weight: 400;
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
        -webkit-touch-callout: none;
        -khtml-user-select: none;
        cursor: none;
    }
    .wrapper {
        position: relative;
        width: 100%;
        height: 100%;
        overflow: hidden;
        background-color: #fff;
        color: #333;
    }
    .page img {
        width: 100%;
        height: 100%;
    }
    .panel {
        position: fixed;
        bottom: 2vh;
        left: 0;
        right: 0;
        text-align: center;
        z-index: 10;
        display: flex;
        align-items: center;
        margin: 0 auto;
        justify-content: center;
    }
    .panel button {
        background-color: #1D74BB;
        color: #fff;
        width: 6vh;
        height: 6vh;
        padding: 1.5vh;
        box-shadow: none;
        border: 0;
        border-radius: 100%;
        margin: 0 0.5vh;
    }
    .panel button:active {
        background-color: #107883;
        opacity: 0.8;
    }
    .panel button svg {
        width: 100%;
        height: 100%;
    }
    .index {
        position: absolute;
        z-index: 1;
        top: 17.1vh;
        left: 2.6vh;
        right: 2.8vh;
        display: flex;
        align-items: flex-start;
    }
    .index .col:nth-child(1) {
        width: 32.5%;
        margin-right: 3.8vh;
    }
    .index .col:nth-child(2) {
        width: 32.5%;
        margin-right: 3.5vh;
    }
    .index .col:nth-child(3) {
        width: 32.5%;
    }
    .index h2 {
        font-weight: 400;
        text-transform: uppercase;
        font-size: 3.7vh;
        letter-spacing: 0.5px;
        margin-top: 0;
        margin-bottom: 2.2vh;
        padding-left: 4vh;
    }
    .index ul {
        padding: 0;
        margin: 0;
        list-style: none;
        padding-left: 2.7vh;
    }
    .index ul li {
        font-size: 2vh;
        letter-spacing: 0.2px;
        border-bottom: 1px solid #333;
        padding-top: 0.5vh;
        padding-bottom: 0.45vh;
        padding-left: 1.2vh;
        min-height: 4.5vh;
        display: flex;
        align-items: center;
        line-height: 1.1;
        position: relative;
    }
    .index ul li:active {
        background-color: rgba(29, 116, 187, 0.95);
        color: #fff;
    }
    .index ul li::before {
        content: '';
        display: block;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        left: -2.7vh;
        width: 1vh;
        height: 1vh;
        background-color: #1D74BB;
    }
    .col:nth-child(3) ul li::before {
        background-color: #107883;
    }
    .fadeout {
        position: absolute;
        z-index: 10;
        background-color: #fff;
        width: 100vw;
        height: 100vh;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        animation-name: fadeout;
        animation-duration: 0.2s;
    }
    @keyframes fadeout {
        from { opacity: 0; }
        to { opacity: 1; }
    }
</style>
