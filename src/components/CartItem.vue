<template>
    <div class="items">
        <slot></slot>
    </div>
</template>
  
<style>
.items {
    display: flex;
    align-items: center;
    text-align: center;
    margin-top: 2rem;
    width: 300px;
    height: 300px;
    border: 3px solid blue;
    line-break: strict;
    line-height: 5pt;
}
</style>