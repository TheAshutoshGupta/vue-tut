<template>
    <div>
        <div id="navbar">
            <div id="lhs">Home</div>
            <div class="rhs">
                <div>Account</div>
                <div class="cart">
                    <q-icon name="shopping_cart" />
                    <div class="cart_count">1</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    #navbar{
        display: flex;
        height:70px;
        align-items: center;
        border-bottom: solid 1px black;
        font-size: 130%;
    }
    #lhs{
        display: flex;
        flex:3;
        align-items: center;
    }
    .rhs
    {
        display: flex;

        flex:7;
        gap:10%;
        align-items: center;
        justify-content: flex-end;
    }
    .cart{
        display: flex;
        align-items: center;

    }
</style>