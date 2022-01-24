<template>
  <div>
    <!-- The v-text directive output works very similarly to the interpolation method -->
    <h1>{{ text }}</h1>
    <!-- same as -->
    <h1 v-text="text"></h1>

    <!-- ============================================================================ -->
    <h1 v-once>This will never change: {{ text }}</h1>

    <!-- ============================================================================ -->
    <h2 v-html="my_html" />

    <!-- ============================================================================ -->
    <a
      v-bind:href="link.url"
      v-bind:target="link.target"
      v-bind:tabindex="link.tabindex"
    >
    {{ link.title }}
    </a>

    <p>This is equivalent to:</p>

    <a
      :href="link.url"
      :target="link.target"
      :tabindex="link.tabindex"
    >
    {{ link.title }}
    </a>

    <!-- ============================================================================ -->
    <h1>Demonstrating v-if, v-else-if and v-else:</h1>
    
    <h1 v-if="condition===111" v-once>Loading...{{ text }} because condition equals 11</h1>

    <h2 v-else-if="condition < 111" v-html="my_html" />

    <a
      v-else
      :href="link.url"
      :target="link.target"
      :tabindex="link.tabindex"
      v-text="link.title"
    />
    
    <!-- ============================================================================ -->
    <h1 v-show="true" v-once>Loading...{{ text }} because v-show is TRUE!</h1>

    <h2 v-show="false" v-html="my_html" />
  </div>
</template>

<script>
export default {
    setup() {
        // v-text
        const text = "Directive text";  // v-text

        // v-html
        const my_html = "Stylise</br>HTML in<br/><b>your data</b>";

        // v-bind
        const link = {
          url: 'https://www.google.com',
          target: '_blank',
          tabindex: '0',
          title: 'Go to Google',
        };

        const condition = 111;

        return { text, my_html, link, condition }
    }
};
</script>

<style>
  h1 { margin: 40px 0 0; font-weight: normal; }
  
  a {
    display: block;
    margin-top: 40px;
  }
</style>
