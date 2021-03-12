<template>
    <v-text>
        <h1>氏名<input placeholder="フルネームで入力してください"></h1>
        <h1>住所<input placeholder="住所"></h1>
        <h1>メールアドレス<input placeholder="メールアドレス"></h1>
        <h1>電話番号<input placeholder="電話番号"></h1>
        <h1>性別
            <label><input type="radio" name="sex" v-model="picked" value="man">男性</label>
            <label><input type="radio" name="sex" v-model="picked" value="woman">女性</label>
            <label><input type="radio" name="sex" v-model="picked" value="other">その他</label></h1>
        <h1>年齢<select v-model="selected">
            <option value="10代">10代</option>
            <option value="20代">20代</option>
            <option value="30代">30代</option>
            <option value="40代">40代</option>
            <option value="50代">50代</option>
            </select></h1>
        <h1>問い合わせ内容<br><textarea v-model="message" placeholder="add multiple lines"></textarea></h1>
    </v-text>
</template>

<script>
export default {
    name: 'contactUs',
    components:{}
};
</script>

