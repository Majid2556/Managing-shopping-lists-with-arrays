# Managing-shopping-lists-with-arrays

let shoppingList = [];

function addItem(item, quantity = 1) {
    shoppingList.push({ item, quantity, date: new Date().toLocaleDateString('fa-IR') });
    console.log(`✅ ${quantity} عدد ${item} به لیست اضافه شد.`);
}

function showList() {
    console.log("📋 لیست خرید:");
    shoppingList.forEach((item, index) => {
        console.log(`${index + 1}. ${item.item} (${item.quantity} عدد) - ${item.date}`);
    });
}

// تست
addItem("شیر", 2);
addItem("نان", 3);
addItem("تخم مرغ");
showList();
