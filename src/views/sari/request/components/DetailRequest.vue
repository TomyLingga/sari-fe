<script setup>
    import { onMounted, ref, defineProps } from 'vue';

    // Variable
    const props = defineProps({
        data_dialog:{
            type:Array
        },
    });
    const datas = props.data_dialog;
    const roles = ref(localStorage.getItem('roles'));

    const loadData = async() => {
        console.log(datas);
    }

    loadData();
</script>
<template>
    <div class="grid pt-2">
        <div class="col-3"><strong>Requestor</strong></div>
        <div class="col-9">: {{ datas.requestor }}</div>
        <div class="col-3"><strong>Position</strong></div>
        <div class="col-9">: {{ datas.jabatan }}</div>
        <div class="col-3"><strong>Phone Number</strong></div>
        <div class="col-9">: {{ datas.nohp }}</div>
        <div class="col-3"><strong>Category</strong></div>
        <div class="col-9">: {{ datas.kategori }}</div>
        <div class="col-3"><strong>Request Type</strong></div>
        <div class="col-9">: {{ datas.permintaan }}</div>
        <div class="col-3"><strong>Necessary</strong></div>
        <div class="col-9"><p style="max-width: 600px;">: {{ datas.keperluan }}</p></div>
        <div class="col-3"><strong>Request Date</strong></div>
        <div class="col-9">: Requested by <span class="font-semibold">{{ datas.requestor }}</span> on <span class="font-semibold">{{ datas.tgl }}</span></div>
        <div class="col-3"><strong>Leader of Requestor</strong></div>
        <div class="col-9">: {{ datas.atasan }}</div>
        <div class="col-3"><strong>SPV/MGR Maintenance</strong></div>
        <div class="col-9">:</div>
        <div class="col-3"><strong>Eksekutor</strong></div>
        <div class="col-9">:</div>
    </div>
</template>