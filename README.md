# TheCashier

a. Nama Aplikasi : TheCashier

b. Fungsionalitas : Menambahkan barang/jasa dan melihat total harga dari barang/jasa

c. 

        public Item(int id, string title, int quantity, string type, double price)
        {
            this.id = id;
            this.title = title;
            this.quantity = quantity;
            this.type = type;
            this.price = price;
            this.subtotal = 0;
        }
        public string getTitle()
        {
            return title;
        }
        public int getQuantity()
        {
            return quantity;
        }
        public string getType()
        {
            return type;
        }
        public double getPrice()
        {
            return price;
        }
        public double getSubTotal()
        {
            subtotal = price * quantity;
            return subtotal;
        }

codingan diatas merupakan sebagian dari class Item.cs. Suatu method yang akan menghandle inputan user mencakup nama barang, jumlah barang, jenis barang (barang/jasa), harga barang dan mendapatkan total harga barang.


        private List<Item> listItem;
        private double total = 0;
        public Calculator()
        {
            this.listItem = new List<Item>();
        }
        public void addItem(Item item)
        {
            this.listItem.Add(item);
            this.total += item.getSubTotal();
        }
        public double getTotal()
        {
            return total;
        }
        public List<Item> getListItem()
        {
            return listItem;
        }


codingan diatas sebagian dari class Calculator.cs, dan konsep single responsibility terdapat didalamnya karena class ini berfungsi menambahkan item yang dimasukkan user kedalam list kemudian aplikasi akan menghitung total harganya.
