# Vue 3 + Vite

This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Assignment
Develop a web application using Vue 3 with the following functionalities:
=> Create a calculator with basic arithmetic operations (+, -, *, /). Implement this functionality within a separate component named 'Calculator'.
    => The calculator component should consist of:
        => Two input fields for entering numeric values.
        => One input field for selecting the arithmetic operation (+, -, *, /).
        => Upon submission, display the result below the submit button.
=> Implement a separate component to fetch and display data from an API.
    => Utilize the following API: https://animechan.xyz/api/random
    => This API returns a JSON object with the following format:
        {
            id: "",
            quote: "",
            anime: "",
            character: ""
       }
   => Display the retrieved JSON object data.




Note: The provided API generates random text upon each call, so keep this in mind during development to avoid confusion.
