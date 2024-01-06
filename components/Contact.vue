<template>
    <v-container>
        <h1>Contact</h1>
        <p>お気軽にご連絡ください。</p>
        <v-form method="POST">
            <v-text-field label="お名前"></v-text-field>
            <v-text-field label="メールアドレス"></v-text-field>
            <v-textarea label="ご用件"></v-textarea>
            <v-btn>送信</v-btn>
        </v-form>
    </v-container>
</template>