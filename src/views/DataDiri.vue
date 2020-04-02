<template>
<div id="app" class="d-flex justify-content-center">
    <div id="tabledd">
        <table class="table text-left table-striped table-responsive">
            <tr>
                <td>Nama Lengkap</td>
                <td>:</td>
                <td>{{ nama }}</td>
            </tr>
            <tr>
                <td>Prodi</td>
                <td>:</td>
                <td>{{ prodi }}</td>
            </tr>
            <tr>
                <td>Tahun Angkatan</td>
                <td>:</td>
                <td>{{ angkatan }}</td>
            </tr>
            <tr>
                <td>Email</td>
                <td>:</td>
                <td><a href="mailto:rabellaazzahra@gmail.com">{{ email }}</a></td>
            </tr>
        </table></div></div>
</template>
<script>
    export default {
        name: 'DataDiri',
        data() {
            return {
                nama: "Rabella Rigustama Az Zahra",
                prodi: "Teknik Informatika",
                angkatan: "2017",
                email: "rabellaazzahra@gmail.com"
            }
        }
    }
</script>