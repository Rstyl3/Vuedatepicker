<template>
    <div class="formWrapper">
        <form>
            <float-label>
              <input name="name" type="text" placeholder="Customer Name">
            </float-label>
            <float-label>
              <input name="email" type="text" placeholder="Email">
            </float-label>
        </form>
    </div>
</template>

<script>

export default {
  name: 'Form'
}
</script>

<style lang="scss" scoped>
.formWrapper{
    width: 30%;
    margin: 0 auto;
    padding: 20px;

    input,
    textarea,
    select {
        margin-bottom: 2em;
        line-height: 1.15;
        font-size: 15px;
        padding: .4em .4em .4em 0;
        width: 80%;
    }
    input:-webkit-autofill {
       box-shadow: 0 0 0 30px white inset;
    }
}
form{
    /deep/ .vfl-label + input {
    padding-left: 0;
    font-size: 100%;
    border: 0;
    border-bottom: 2px solid #aaa;
    transition: border 0.2s;
    }
    /deep/ .vfl-label {
       text-transform: uppercase;
       right: auto;
       padding-left: 55px;
    }
    /deep/ .vfl-label-on-focus {
    color: #ff851b;
    }
    /deep/ .vfl-label-on-input {
       top: -1em;
    }
    /deep/ .vfl-label-on-focus + input  {
    border-bottom: 2px solid #ff851b;
    }
}
</style>
