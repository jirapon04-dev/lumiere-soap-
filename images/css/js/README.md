
let cart = [];

function addToCart(sku, name, price) {
  const item = cart.find(product => product.sku === sku);

  if (item) {
    item.quantity++;
  } else {
    cart.push({
      sku: sku,
      name: name,
      price: price,
      quantity: 1
    });
  }

  showCart();
}

function showCart() {
  const cartList = document.getElementById("cart-list");
  const totalText = document.getElementById("total");

  cartList.innerHTML = "";
  let total = 0;

  cart.forEach(item => {
    const subtotal = item.price * item.quantity;
    total += subtotal;

    const row = document.createElement("p");
    row.textContent =
      `${item.name} x ${item.quantity} = ${subtotal} บาท`;

    cartList.appendChild(row);
  });

  totalText.textContent = total;
}

function checkout() {
  if (cart.length === 0) {
    alert("กรุณาเลือกสินค้าก่อนสั่งซื้อ");
    return;
  }

  const order = {
    orderId: "LS" + Date.now(),
    items: cart,
    total: cart.reduce(
      (sum, item) => sum + item.price * item.quantity, 0
    )
  };

  alert(
    "สร้างรายการสั่งซื้อแล้ว\n" +
    "เลขที่คำสั่งซื้อ: " + order.orderId +
    "\nยอดรวม: " + order.total + " บาท"
  );

  console.log("Order:", order);
}
