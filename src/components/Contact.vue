<template>
    <div class="contact-wrapper mt-[100px]" id="join">
        <div class="grid grid-cols-10 xs:gap-10 items-center">
            <div class="sm:col-span-6 col-span-10">
                <Title>Готовы присоединиться и развиваться вместе c нами?</Title>
                <Description>Заполните форму, и мы свяжемся c вами!</Description>

                <form class="form" @submit="submitHandler">
                    <div class="form-control xs:grid xs:grid-cols-2 gap-3">
                        <div class="mt-5">
                            <Input label="Имя"/>
                        </div>
                        <div class="mt-5">
                            <Input label="Фамилия"/>
                        </div>
                        <div class="mt-5">
                            <Input label="Номер телефона"/>
                        </div>
                        <div class="mt-5">
                            <Select label="Направление" class="w-full" :className="'bg-white border border-slate-300'" :options="directions"/>
                        </div>
                        <div class="mt-5">
                            <Select label="Город" class="w-full" :className="'bg-white border border-slate-300'" :options="cities" />
                        </div>
                        <div class="mt-5">
                            <Select label="Район" class="w-full" :className="'bg-white border border-slate-300'" :options="districts"/>
                        </div>
                    </div>
                    <Button class="mx-auto mt-12 block px-12" type="submit">Отправить</Button>
                </form>

            </div>
            <div class="col-span-4 hidden sm:block">
                <img src="../assets/images/contact.png" alt="">
            </div>
        </div>
    </div>
</template>
<script>
import { Title, Description, Input, Select, Button } from '../ui-components';
export default {
    components: {Title, Description, Input, Select, Button},
    data() {
        return {
            directions: [
                {id: 1, value: ''},
                {id: 2, value: 'A'},
                {id: 3, value: 'B'},
            ],
            cities: [
                {id: 1, value: ''},
                {id: 2, value: 'Tashkent'},
                {id: 3, value: 'Samarkand'},
            ],
            districts: [
                {id: 1, value: ''},
                {id: 2, value: 'Sergeli'},
                {id: 3, value: 'Uchtepa'},
                {id: 4, value: 'Chilonzor'},
            ],
        }
    },
    methods: {
        submitHandler(e) {
            e.preventDefault();
            alert("Your information sent!")            
        }
    }

}
</script>
<style scoped> 
    select{
        background: #fff!important;
    }
</style>