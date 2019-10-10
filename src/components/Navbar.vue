<template>
    <v-app-bar app color = "primary" dark>
        <v-toolbar-title>Localización Barranquilla</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn 
        v-for="link in links"
        :key ="link"
        text
        rounded
        @click="move(key)"
        >{{link}}
        </v-btn>
        
    </v-app-bar>
</template>

<script>
export default {
    data: () =>({
       links: [
           'Home','Register','Login'
       ]
    })
}
</script>
