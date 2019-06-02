<template>

    <div class="basket">
        <h2>Ваша корзина</h2>
        <h3>Товары резервируются на ограниченное время</h3>

        <div class="basket_table">
            <div class="basket_table-head">
                <div class="basket_table-head_item">Фото</div>
                <div class="basket_table-head_item biggest">Наименование</div>
                <div class="basket_table-head_item">Размер</div>
                <div class="basket_table-head_item">Количество</div>
                <div class="basket_table-head_item">Стоимость</div>
                <div class="basket_table-head_item">Удалить</div>
            </div>
            <div class="basket_table-body">
                <div class="basket_table-body_item">фото</div>
                <div class="basket_table-body_item biggest">
                    <div class="title">Название</div>
                    <div class="vendor_code">Артикул</div>
                </div>
                <div class="basket_table-body_item">размер</div>
                <div class="basket_table-body_item count">
                    <input type="number" name="count" value="1"/>
                    <div class="control">
                        <span class="plus">+</span>
                        <span class="minus">-</span>
                    </div>
                </div>
                <div class="basket_table-body_item">стоимость</div>
                <div class="basket_table-body_item">х</div>
            </div>
            <div class="basket_table-footer">
                <div></div>
                <div></div>
                <div></div>
                <div>Итого:</div>
                <div class="summary">12500руб.</div>
                <div></div>
            </div>
        </div>

        <div class="basket_zigzag">
            <div></div>
            <div></div>
            <div></div>
        </div>

        <form>
            <h2>Адрес доставки</h2>
            <h3>Все поля обязательны для заполнения</h3>

            <div class="form_body">

                <label for="delivery" class="long">
                    <div>Выберите вариант доставки</div>
                    <select id="delivery">
                        <option>Курьерская служба - 500руб.</option>
                        <option>Самовывоз - 250руб.</option>
                        <option>Почта Росии - 150руб.</option>
                    </select>
                </label>

                <label for="first_name">
                    <div>Имя</div>
                    <input type="text" id="first_name" name="first_name"/>
                </label>

                <label for="last_name">
                    <div>Фамилия</div>
                    <input type="text" id="last_name" name="last_name"/>
                </label>

                <label for="address" class="long">
                    <div>Адрес</div>
                    <input type="text" id="address" name="address"/>
                </label>

                <label for="city">
                    <div>Город</div>
                    <input type="text" id="city" name="city"/>
                </label>

                <label for="zip_code">
                    <div>Индекс</div>
                    <input type="text" id="zip_code" name="zip_code"/>
                </label>

                <label for="phone">
                    <div>Телефон</div>
                    <input type="text" id="phone" name="phone"/>
                </label>

                <label for="email">
                    <div>Email</div>
                    <input type="text" id="email" name="email"/>
                </label>

            </div>
        </form>

        <div class="basket_zigzag">
            <div></div>
            <div></div>
            <div></div>
        </div>

        <form>
            <h2>Варианты оплаты</h2>
            <h3>Все поля обязательны для заполнения</h3>

            <div class="summary">
                <div>
                    <span>Стоимость:</span>
                    <span>123123руб.</span>
                </div>
                <div>
                    <span>Доставка:</span>
                    <span>123руб.</span>
                </div>
                <div class="total">
                    <span>Итого:</span>
                    <span>2342342324руб.</span>
                </div>
            </div>
        </form>
    </div>

</template>

<script>
    export default {
        name: "Basket"
    }
</script>

<style scoped>

    .basket h2 {
        text-align: center;
        margin-top: 6rem;
        text-transform: uppercase;
        font-size: 2rem;
        margin-bottom: .6rem;
    }

    .basket h3 {
        text-align: center;
        color: grey;
        font-style: italic;
        margin-top: 0;
    }

    .basket .basket_table {
        margin-top: 6rem;
        color: grey;
        display: table;
        width: 100%;
        border-collapse: collapse;
    }

    .basket .basket_table .basket_table-head {
        display: table-row;
    }

    .basket .basket_table .basket_table-head .basket_table-head_item {
        display: table-cell;
        width: calc(100% / 6);
        border-bottom: 2px solid lightgrey;
        padding-bottom: 10px;
    }

    .basket .basket_table .basket_table-body {
        display: table-row;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item {
        display: table-cell;
        width: calc(100% / 6);
        border-bottom: 2px solid lightgrey;
        padding-bottom: 10px;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item:first-child {
        height: 95px;
        align-items: center;
        display: flex;
        justify-content: center;
        width: 100%;
        margin: 5px;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item {
        color: black;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item.count {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 100%;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item input {
        border: none;
        width: 20px;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item input::-webkit-inner-spin-button {
        display: none;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item .control {
        display: flex;
        flex-direction: column;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item .control span {
        width: 10px;
        height: 10px;
        background-color: black;
        color: white;
        font-size: 10px;
        text-align: center;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item .control span:first-child {
        margin-bottom: 2px;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item input:focus {
        outline: none;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item .vendor_code {
        color: grey;
        font-size: .8rem;
    }

    .basket .basket_table .basket_table-body .basket_table-body_item:last-child {
        text-align: center;
    }

    .basket .basket_table .basket_table-footer {
        display: table-row;
        background-color: rgba(27, 70, 80, 0.1);
    }

    .basket .basket_table .basket_table-footer div {
        display: table-cell;
        padding: 10px 0;
    }

    .basket .basket_table .basket_table-footer div.summary {
        color: orange;
        font-weight: bold;
    }

    .biggest {
        width: 50% !important;
    }

    .basket_zigzag {
        display: flex;
        width: 100%;
        flex-direction: row;
        justify-content: center;
        margin: 6rem 0;
    }

    .basket_zigzag div {
        border-right: 1px solid orange;
        border-bottom: 1px solid orange;
        width: 15px;
        height: 15px;
        transform: rotate(45deg);
        margin-right: 5px;
    }

    .basket form{
        border: 2px solid lightgrey;
        margin: 10px;
        padding-bottom: 6rem;
    }

    .basket form .form_body{
        display: flex;
        flex-direction: row;
        width: 60%;
        align-items: center;
        flex-wrap: wrap;
        margin: 0 auto;
    }

    .basket form .form_body label{
        width: 45%;
        margin-bottom: 2rem;
    }

    .basket form .form_body label:nth-child(2),
    .basket form .form_body label:nth-child(5),
    .basket form .form_body label:nth-child(7){
        margin-right: auto;
    }

    .basket form .form_body label.long{
        width: 100%;
    }

    .basket form .form_body label > *{
        width: 100%;
    }

    .basket form .form_body label > div{
        color: grey;
        text-transform: uppercase;
        font-size: .6rem;
        margin-bottom: 3px;
    }

    .basket form .form_body label > input,
    .basket form .form_body label > select{
        padding: 5px;
        border: 1px solid lightgrey;
        border-radius: 2px;
        background-color: transparent;
    }

    .basket form .form_body label > input:focus{
        outline: none;
    }

    form > .summary{
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    form > .summary > div{
        display: flex;
        width: 100%;
        margin-bottom: 10px;
        color: grey;
    }

    form > .summary > div span:first-child{
        width: 50%;
        display: flex;
        justify-content: flex-end;
    }

    form > .summary > div span:last-child{
        width: 50%;
        display: flex;
        justify-content: flex-start;
        padding-left: 10px;
    }

    form > .summary > div.total{
        color: orange;
    }

</style>