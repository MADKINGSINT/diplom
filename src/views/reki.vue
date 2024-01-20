<template>
    <div class="box">
        <p class="text text1"></p>
        <p class="text">Название: ООО "Эра Карс"<br>

    Юр.адрес: 187021, Ленинградская область, Тосненский р-н,<br>

    городской посёлок Фёдоровское, ул. Шоссейная, д. 29Г, помещение 1, офис 1 <br>

    Факт.адрес: 187021, Ленинградская область, Тосненский р-н, <br>

    городской посёлок Фёдоровское, ул. Шоссейная, д. 29Г, помещение 1, офис 1 <br>

    ОГРН : 1204700011306 <br>

    ИНН : 4716047303 <br>

    КПП : 471601001 <br>

    ОКПО : 44631380 <br>

    ОКАТО : 41248567000 <br>

    Р/сч.: 40702810400000004084 Филиал Центральный Банк ВТБ (ПАО) г. Москва  <br>

    Кор/сч.: 30101810145250000411 <br>

    БИК : 044525411 <br>

    Тел.: 8 (921) 585-03-50 <br>

    Ген. директор: Смирнов Игорь Александрович <br>

    Гл. бухгалтер: Смирнов Игорь Александрович <br>

    Эл.почта: info@eracars.ru</p>
    </div>
</template>

<script>
export default {
    
}
</script>
<style lang="scss">
    .box{
        display: flex;
        
        width: 100%;
        height: 90vh;
        background-image: url(../assets/img/камаз.jpg);
        background-size: cover;
        object-fit: cover;
        background-repeat: no-repeat;
        position: fixed;
    }
    .text{
        font-weight: bold;
        font-family: Arial;
        width: 100%;
        display: flex;
        color: #fff;
        justify-content: center;
        align-items: center;
        align-content: center;
    }
    @media only screen and (max-width: 576px) {
        .text{
            font-size: 14px;
            justify-content: center;
            width: 70%;
            padding-left: 15%;
            padding-right: 15%;
        }
        .text1{
            display: none;
        }
    }
</style>