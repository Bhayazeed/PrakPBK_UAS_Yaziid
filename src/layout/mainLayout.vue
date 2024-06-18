<template>
    <q-layout view="hHh lpR fFf">

        <q-header elevated class="bg-primary text-white" >
            <q-toolbar>
                <q-toolbar-title align="left">
                    Weather API 
                </q-toolbar-title>
            </q-toolbar>
        </q-header>
        <q-page-container>
            <router-view />
        </q-page-container>
        <q-footer elevated align="left" class="bg-secondary text-white">
            <q-toolbar>
                <q-toolbar-title>
                    M.Bhayaziid Amalin - 223510209 4E
                </q-toolbar-title>
            </q-toolbar>
        </q-footer>
    </q-layout>
</template>