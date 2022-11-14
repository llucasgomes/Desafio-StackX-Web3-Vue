<template>
    <div class="p-[20px] w-[530px] h-[150px] rounded-lg bg-[#27272a] border-solid border-[2px] border-[#9d4b00] flex items-center">   
        <ul class="flex w-full h-full flex-wrap flex-col px-[2px] items-start"  >
            <li class="pl-[10px] mx-[10px]  text-white" v-for="(item) in Tecnologias">{{item}}</li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            Tecnologias:["Javascript","React",'Vue js','Tailwind CSS','Styled Components','Saas',"Node",'TypeScript',"Angular","Java"],

        }
    }
    
}
</script>