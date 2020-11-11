<template>
  <div class="container">
      Work Log is a log of tasks I completed on day to day basis.
      <br/><br/>
      <input type="password" class="inputBox" id="exampleInputPassword1" placeholder="Password to view work log">
      <br/>
      <button type="submit" class="btn btn-primary mb-2">Enter</button>
  </div>
</template>

<script>

export default {
    components: {
    },
    data () {
        return {

        }
    },
    mounted () {
    }
}
</script>

<style scoped>
    .container {
        padding-top: 160px;
        margin: 20px;
        flex: 1;
        flex-direction: column;
    }
    .inputBox {
        max-width: 300px;
        box-sizing: border-box;
        margin: 0;
        font-family: inherit;
        overflow: visible;
        display: block;
        width: 100%;
        padding: .375rem .75rem;
        font-size: 1rem;
        line-height: 1.5;
        color: #495057;
        background-color: #fff;
        background-clip: padding-box;
        border: 1px solid #ced4da;
        border-radius: .25rem;
        /* transition: border-color .15s ease-in-out,box-shadow .15s ease-in-out; */
    }
    .btn {
        max-width: 100px;
        -webkit-box-direction: normal;
        box-sizing: border-box;
        margin: 0;
        font-family: inherit;
        overflow: visible;
        text-transform: none;
        display: inline-block;
        font-weight: 400;
        text-align: center;
        white-space: nowrap;
        vertical-align: middle;
        user-select: none;
        border: 1px solid transparent;
        padding: .375rem .75rem;
        font-size: 1rem;
        line-height: 1.5;
        border-radius: .25rem;
        transition: color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out,box-shadow .15s ease-in-out;
        color: #fff;
        background-color: #20c997;
        border-color: #20c997;
        margin-bottom: .5rem!important;
        cursor: pointer;
    }
</style>