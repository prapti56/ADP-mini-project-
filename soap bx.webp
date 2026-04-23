let cart = [];

/* ✅ ADD TO CART */
document.querySelectorAll(".cart").forEach(btn => {
  btn.addEventListener("click", () => {
    let card = btn.closest(".card");
    let name = card.querySelector("h2").innerText;
    let price = card.querySelector(".price").innerText;

    cart.push({ name, price });

    alert(name + " added to cart ✅");
    console.log("Cart:", cart);
  });
});

/* ✅ SEARCH FILTER */
document.getElementById("search").addEventListener("keyup", function () {
  let value = this.value.toLowerCase();
  let cards = document.querySelectorAll(".card");

  cards.forEach(card => {
    let title = card.querySelector("h2").innerText.toLowerCase();

    if (title.includes(value)) {
      card.style.display = "block";
    } else {
      card.style.display = "none";
    }
  });
});

/* ✅ BUY NOW (WhatsApp Integration) */
function buyNow(button) {
  let card = button.closest(".card");
  let name = card.querySelector("h2").innerText;
  let price = card.querySelector(".price").innerText;

  let phone = "919022161744"; // 🔴 PUT YOUR NUMBER

  let message = `Hello, I want to buy:\n${name}\n${price}`;
  let url = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;

  window.open(url, "_blank");
}



