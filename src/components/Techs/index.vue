<template>
    <div class="w-[503px] h-[103px] rounded-lg bg-[#27272a] border-solid border-[2px] border-[#9d4b00] flex items-center justify-center">
        
        <ul class="flex ">
            <li class="inline-block text-white" v-for="(item) in Tecnologias">{{item}}</li>

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