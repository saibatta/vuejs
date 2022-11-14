<template>
  <div class="hello">
    <p>
      {{ msg }}--<strong>{{ name }}</strong>
    </p>
    <hr />
    <p><u>Text Binding with v-text & v-html : </u></p>
    <div v-text="textInput"></div>
    <br />
    <div v-html="htmlInput"></div>
    <div v-html="htmlAlert"></div>

    <hr />
    <p><u>Attribute Binding with v-text & v-html : </u></p>
    <div v-bind:id="vbindtextId">V Bind text Id to identify the div id</div>
    <br />
    <button v-bind:disabled="isDisabled">Bind</button>

    <hr />
    <p>Style attribute examples</p>
    <div class="underlined">static text undelined with the class</div>
    <div v-bind:class="dynamicClassEnabled">dynamic text with the class</div>
    <div class="underlined" v-bind:class="dynamicClassEnabled">
      dynamic text with static underline class
    </div>
    <div v-bind:class="isDynamicClass ? 'dynamicClassPass' : 'dynamicClassFail'">
      Dynaic text with terniory condition check
      <strong> -- {{ isDynamicClass }}</strong>
    </div>
    <div v-bind:class="['underlined', 'dynamicClassPass']">
      combining two class like array ['underlined','dynamicClassPass']
    </div>

    <div v-bind:class="[
      'underlined',
      isDynamicClass ? 'dynamicClassPass' : 'dynamicClassFail',
    ]">
      combining two class like array ['underlined',isDynamicClass?'':'']
    </div>
    <div v-bind:class="{
      dynamicClassPass: !isDynamicClass,
    }">
      Object format class checking
    </div>



    <hr />
    <p>v-bind:style attribute examples</p>
    <div v-bind:style="{ color: 'red' }">v-bind:style text</div>
    <div v-bind:style="[styledObjA, styledObjB]">v-bind:style text</div>

    <hr />
    <p>v-bind:name short hand to :name</p>
    <div :class="{ dynamicClassPass: !isDynamicClass }"> Short hand v-bind to <strong>:name</strong></div>
  </div>
</template>

<script>
export default {
  name: "TextBinding",
  props: {
    msg: String,
  },
  data() {
    return {
      name: "TextBinding Component",
      textInput: "Normal Vue text input with v-text",
      htmlInput: "<b>HTML Vue  text binding with v-html</b>",
      htmlAlert: `<a href="#" onclick="alert('link clked')"> Link</a>`,
      vbindtextId: "VBindtextId",
      isDisabled: true,
      dynamicClassEnabled: "dynamicClass",
      isDynamicClass: false,
      styledObjA: {
        color: "yellow",
        "font-size": "20px",
      },
      styledObjB: {
        background: "green",
        "font-size": "20px",
        padding: "10px",
      },
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.underlined {
  text-decoration: underline;
  color: rgb(207, 117, 117);
}

.dynamicClass {
  color: rgb(128, 0, 124);
  font-size: 28px;
}

.dynamicClassPass {
  color: green;
  font-size: 28px;
}

.dynamicClassFail {
  color: red;
  font-size: 28px;
}
</style>
