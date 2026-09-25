<template>
  <nav>
    <h2>BlueShop</h2>

    <div>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/product">Product</RouterLink>
      <RouterLink to="/about">About</RouterLink>
            <RouterLink to="/contact">contact</RouterLink>

    </div>

    <button>🛍️ Shop</button>
  </nav>
</template>


<style scoped>
nav{
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:15px 8%;
  background:#fff;
  box-shadow:0 3px 15px #e9d5ff;
}

h2{color:#7c3aed;margin:0}

div{display:flex;gap:20px}

a{
  text-decoration:none;
  color:#6b5b7b;
  font-weight:bold;
}

a:hover{color:#7c3aed}

button{
  border:0;
  padding:9px 15px;
  border-radius:20px;
  background:#7c3aed;
  color:white;
  font-weight:bold;
}
</style>