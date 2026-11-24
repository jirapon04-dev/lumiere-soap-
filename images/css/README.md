
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #fffaf7;
  color: #443b36;
}

header {
  background: #f4e5dc;
  text-align: center;
  padding: 28px 15px;
}

header h1 {
  margin: 0;
  color: #795b50;
}

nav {
  background: #fff;
  padding: 14px;
  text-align: center;
}

nav a {
  color: #795b50;
  text-decoration: none;
  margin: 0 12px;
}

.banner {
  text-align: center;
  padding: 45px 15px;
  background: #f8eee8;
}

.products {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 24px;
  max-width: 850px;
  margin: 30px auto;
  padding: 15px;
}

.product {
  background: white;
  padding: 18px;
  text-align: center;
  border-radius: 14px;
  box-shadow: 0 3px 12px #00000010;
}

.product img {
  width: 100%;
  height: 210px;
  object-fit: cover;
  border-radius: 10px;
}

button {
  background: #947366;
  color: white;
  border: none;
  padding: 11px 20px;
  border-radius: 8px;
  cursor: pointer;
}

button:hover {
  background: #705448;
}

#cart {
  max-width: 850px;
  margin: 25px auto;
  padding: 20px;
  background: white;
  border-radius: 12px;
}

footer {
  background: #f4e5dc;
  padding: 22px;
  text-align: center;
  margin-top: 40px;
}
