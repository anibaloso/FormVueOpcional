<script>
export default {
    name: 'FormComponent',
    data() {
        return {
            titulo: '',
            eleccionEmoji: '',
            emoji: {
                'profesor': '👨🏽‍🏫',
                'investigador': '🕵🏽‍♀️',
                'policia': '👮🏽‍♂️',
                'brujo': '🧙🏽‍♂️'
            },
            apreciacion: '',
            competencias: [],
            opinion: ''
        }
    }
}
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-6">
                <div class="container">
                    <div class="row">
                        <div class="col">
                            <label>Título:</label>
                            <input v-model="titulo" />
                        </div>
                    </div>
                    <div class="row">
                        <div class="col">
                            <label>Emoji:</label>
                            <select v-model="eleccionEmoji">
                                <option value="profesor">{{ emoji.profesor }}</option>
                                <option value="investigador">{{ emoji.investigador }}</option>
                                <option value="policia">{{ emoji.policia }}</option>
                                <option value="brujo">{{ emoji.brujo }}</option>
                            </select>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col">
                            <label>Apreciación:</label>
                            <input type="radio" id="regular" v-model="apreciacion" value="regular">
                            <label for="regular">Regular</label>
                            <input type="radio" id="Bien" v-model="apreciacion" value="Bien">
                            <label for="Bien">Bien</label>
                            <input type="radio" id="Muy-bien" v-model="apreciacion" value="Muybien">
                            <label for="Muy-bien">Muy bien</label>
                            <input type="radio" id="Increible" v-model="apreciacion" value="Increible">
                            <label for="Increible">Increible</label>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col">
                            <label>Competencias: </label>
                            <ul>
                                <li><input type="checkbox" v-model="competencias" value="Morfología de un componente">
                                    Morfología de
                                    un componente</li>
                                <li><input type="checkbox" v-model="competencias" value="Directivas"> Directivas</li>
                                <li><input type="checkbox" v-model="competencias"
                                        value="One-Way y Two-Way data binding"> One-Way y
                                    Two-Way data binding</li>
                                <li><input type="checkbox" v-model="competencias" value="Estado"> Estado</li>
                                <li><input type="checkbox" v-model="competencias" value="El Patrón ded diseño MVVM"> El
                                    Patrón ded
                                    diseño MVVM</li>
                            </ul>

                        </div>
                    </div>
                    <div class="row">
                        <div class="col">
                            <label>Opinion: </label>
                            <textarea v-model="opinion"></textarea>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-6 mx-auto text-center" id="formulario">
                <div class="row">
                    <div class="col-12">
                        <label id="icono">{{ emoji[eleccionEmoji] }}</label>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <h3>{{ titulo }}</h3>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <h4>Y me parece {{ apreciacion }}</h4>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <h4>He aprendido:</h4>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <h4>{{ competencias }}</h4>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <h5>Mi opinion hasta ahora del framework es:</h5>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <p>{{ opinion }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>


</template>

<style scoped>
.row {
    border-bottom: 2px solid white;
    margin-bottom: 1rem;
    padding-bottom: 2rem;
}

label {
    margin-right: 1rem;
}

li {
    list-style: none;
}

#formulario {
    background-color: white;
    color: black;
    
}

#icono {
    font-size: xx-large;
}
</style>