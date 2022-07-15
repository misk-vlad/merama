<template>
    <div>
        <h1>Продукты</h1>
        <ul>
            <li>
                <nuxt-link :to="'products/1'"/>
                <nuxt-link to="products/2"/>
                <nuxt-link to="products/3"/>
                <nuxt-link to="products/4"/>
                <nuxt-link to="products/5"/>
            </li>
        </ul>
    </div>
</template>