<template>
  <VAppBar fixed shadow="sm" size="auto">
    <div class="container w-3/4 flex flex-row mx-auto justify-between">
      <VLogo />
      <div class="text-base font-bold p-2">
        <ul class="flex flex-row">
          <li>Home</li>
          <li>About</li>
          <li>Services</li>
          <li>Blog</li>
          <li>Contact</li>
        </ul>
      </div>
    </div>
  </VAppBar>
</template>

<style>
li {
  padding-left: 50px;
  cursor: pointer;
}
</style>