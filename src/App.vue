<script setup>
  import Button from "@/components/Buttons.vue";

  const sampleCodes = {
    default: '<Button />',
    outlineBtn: '<Button variant="outline" />',
    textBtn: '<Button variant="text" />',
    noShadow: '<Button disableShadow />',
    disabledBtn: '<Button disabled />',
    disabledTextBtn: '<Button variant="text" disabled />',
    iconStartBtn: '<Button startIcon="local_grocery_store" />',
    iconEndBtn: '<Button endIcon="local_grocery_store" />',
    smBtn: '<Button size="sm" />',
    mdBtn: '<Button size="md" />',
    lgBtn: '<Button size="lg" />',
    colorDefaultBtn: '<Button color="default" />',
    colorPrimaryBtn: '<Button color="primary" />',
    colorSecondaryBtn: '<Button color="secondary" />',
    colorDangerBtn: '<Button color="danger" />',
  }
</script>

<template>
  <main>
    <h1>Buttons</h1>
    <pre><code>{{ sampleCodes.default }}</code></pre>
    <Button />

    <pre><code>{{ sampleCodes.outlineBtn }}</code></pre>
    <Button variant="outline" />

    <pre><code>{{ sampleCodes.textBtn }}</code></pre>
    <Button variant="text" />

    <pre><code>{{ sampleCodes.noShadow }}</code></pre>
    <Button disableShadow color="primary" />

    <ul class="flex no-list my-20">
      <li>
        <pre><code>{{ sampleCodes.disabledBtn }}</code></pre>
        <Button disabled />
      </li>
      <li>
        <pre><code>{{ sampleCodes.disabledTextBtn }}</code></pre>
        <Button variant="text" disabled />
      </li>
    </ul>

    <ul class="flex no-list my-20">
      <li>
        <pre><code>{{ sampleCodes.iconStartBtn }}</code></pre>
        <Button startIcon="local_grocery_store" color="primary" />
      </li>
      <li>
        <pre><code>{{ sampleCodes.iconEndBtn }}</code></pre>
        <Button endIcon="local_grocery_store" color="primary" />
      </li>
    </ul>

    <ul class="flex no-list my-20">
      <li>
        <pre><code>{{ sampleCodes.smBtn }}</code></pre>
        <Button size="sm" color="primary" />
      </li>
      <li>
        <pre><code>{{ sampleCodes.mdBtn }}</code></pre>
        <Button size="md" color="primary" />
      </li>
      <li>
        <pre><code>{{ sampleCodes.lgBtn }}</code></pre>
        <Button size="lg" color="primary" />
      </li>
    </ul>

    <ul class="flex no-list my-20">
      <li>
        <pre><code>{{ sampleCodes.colorDefaultBtn }}</code></pre>
        <Button color="default" />
      </li>
      <li>
        <pre><code>{{ sampleCodes.colorPrimaryBtn }}</code></pre>
        <Button color="primary" />
      </li>
      <li>
        <pre><code>{{ sampleCodes.colorSecondaryBtn }}</code></pre>
        <Button color="secondary" />
      </li>
      <li>
        <pre><code>{{ sampleCodes.colorDangerBtn }}</code></pre>
        <Button color="danger" />
      </li>
    </ul>
  </main>
</template>

<style>
@import './assets/base.css';

h1 {
  font-size: 24px;
  font-weight: 500;
  margin-bottom: 28px;
}

code {
  font-family: var(--ff-ubuntu);
  font-weight: 400;
}

.flex {
  display: flex;
  column-gap: 125px;
}
.no-list {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
.my-20 {
  margin-top: 20px;
  margin-bottom: 20px;
}

</style>
