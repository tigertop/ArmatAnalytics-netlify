<template>
    <div>
        <h1>Coming Soon</h1>
        <p>Our website is under construction. Please check back again soon.</p>
    </div>
</template>

<script>
export default {
  name: 'Empty',
  layout: "empty"
};
</script>

<style scoped>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  border: 0;
}
html, body{
  width: 100%;
  height: 100%;
  font-family: Arial,"Helvetica Neue",Helvetica,sans-serif;
  font-size: 14px;
  line-height: 21px;
  color: gray;
  background: white no-repeat center center fixed;
  background-size: cover;
}
div{
  max-width: 360px;
  min-width: 180px;
  margin: auto;
  padding: 20px;
  position: relative;
  top: 50%;
  transform: translateY(-50%);
  background-color: white;
}
h1{
  margin-bottom: 20px;
}
</style>
