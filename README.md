Görev 1. Kullanıcı hesabı

Bu görevi task-1.js dosyasında çalıştırın.

Geliştirici ayrılmadan önce, yemek dağıtım hizmetimiz için kullanıcı hesaplarını yönettiğimiz kaynak kodunu hackledi. Nesnenin özelliklerine erişirken eksik olan this ifadesini değiştirerek customer nesnesinin metodlarını yeniden düzenleyin.

Bu başlangıç kodunu kullanın ve yeniden düzenleyin. Nesneyi tanımladıktan sonra yöntem çağrılarını ekleyin. Çalışmalarının sonuçları konsolda görüntülenecektir. Lütfen orada herhangi bir değişiklik yapmayın.

const customer = {
username: "Mango",
balance: 24000,
discount: 0.1,
orders: ["Burger", "Pizza", "Salad"],
// Change code below this line
getBalance() {
return balance;
},
getDiscount() {
return discount;
},
setDiscount(value) {
discount = value;
},
getOrders() {
return orders;
},
addOrder(cost, order) {
balance -= cost - cost \* discount;
orders.push(order);
},
// Change code above this line
};

customer.setDiscount(0.15);
console.log(customer.getDiscount()); // 0.15
customer.addOrder(5000, "Steak");
console.log(customer.getBalance()); // 19750
console.log(customer.getOrders()); // ["Burger", "Pizza", "Salad", "Steak"]
//////////////////////////////////////////////////////////////////////

Görev 2. Depo

Bu görevi task-2.js dosyasında çalıştırın.

Mal deposunu yönetmek için nesneler oluşturacak bir Storage sınıfı oluşturun. Sınıf yalnızca bir argüman bekler - oluşturulan nesneye items özel özelliğinde yazılan ilk mal dizisi.

Aşağıdaki sınıf yöntemlerini tanımlayın:

getItems() - items özel özelliğindeki mevcut öğelerin bir dizisini döndürür.
addItem(newItem) - yeni bir öğe newItem kabul eder ve nesnenin items özel özelliğindeki öğeler dizisine ekler.
removeItem(itemToRemove) - itemToRemove öğesinin adını içeren bir dize alır ve nesnenin items özel özelliğindeki öğeler dizisinden kaldırır.
Aşağıdaki kodu örnek başlatma ve yöntem çağrılarıyla birlikte alın ve çalışmanın doğruluğunu kontrol etmek için sınıf bildiriminden sonra yapıştırın. Konsol, çalışmalarının sonuçlarını gösterecektir. Lütfen orada herhangi bir değişiklik yapmayın.

const storage = new Storage(["Nanitoids", "Prolonger", "Antigravitator"]);
console.log(storage.getItems()); // ["Nanitoids", "Prolonger", "Antigravitator"]
storage.addItem("Droid");
console.log(storage.getItems()); // ["Nanitoids", "Prolonger", "Antigravitator", "Droid"]
storage.removeItem("Prolonger");
console.log(storage.getItems()); // ["Nanitoids", "Antigravitator", "Droid"]
////////////////////////////////////////////////////////////////////////

Görev 3. String birleştirme

Bu görevi task-3.js dosyasında çalıştırın.

Bir initialValue parametresi alan bir StringBuilder sınıfı yazın - oluşturulan nesnenin value özel özelliğine yazılan rastgele bir dize.

Aşağıdaki sınıf metodlarını tanımlayın:

getValue() - value özel özelliğinin geçerli değerini döndürür.
padEnd(str) - str (dize) parametresini alır ve bu metodu çağıran nesnenin value özel özelliğinin değerinin sonuna ekler.
padStart(str) - str (string) parametresini alır ve bu metodu çağıran nesnenin value özel özelliğinin değerinin başlangıcına ekler.
padBoth(str) - str (dize) parametresini alır ve bu yöntemi çağıran nesnenin value özel özelliğinin değerinin başına ve sonuna ekler.
Aşağıdaki kodu örnek başlatma ve metodlarıyla birlikte alın ve çalışmanın doğruluğunu kontrol etmek için sınıf tanımlanmasından sonra yapıştırın. Konsol, çalışmalarının sonuçlarını gösterecektir. Lütfen orada herhangi bir değişiklik yapmayın.

const builder = new StringBuilder(".");
console.log(builder.getValue()); // "."
builder.padStart("^");
console.log(builder.getValue()); // "^."
builder.padEnd("^");
console.log(builder.getValue()); // "^.^"
builder.padBoth("=");
console.log(builder.getValue()); // "=^.^="
