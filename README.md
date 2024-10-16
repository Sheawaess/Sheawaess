import React from 'react';
import { Search, ShoppingCart, Menu } from 'lucide-react';

export default function TokoSepatuOnlineMockup() {
  return (
    <div className="flex flex-col min-h-screen">
      <header className="bg-blue-600 text-white p-4">
        <div className="container mx-auto flex justify-between items-center">
          <h1 className="text-2xl font-bold">ShoesParadise</h1>
          <div className="flex items-center space-x-4">
            <Search />
            <ShoppingCart />
            <button className="bg-white text-blue-600 px-4 py-2 rounded">Login</button>
          </div>
        </div>
      </header>

      <nav className="bg-blue-500 text-white p-2">
        <div className="container mx-auto flex justify-between items-center">
          <Menu className="md:hidden" />
          <ul className="hidden md:flex space-x-4">
            <li>Beranda</li>
            <li>Pria</li>
            <li>Wanita</li>
            <li>Anak-anak</li>
            <li>Promo</li>
          </ul>
        </div>
      </nav>

      <main className="flex-grow container mx-auto p-4">
        <h2 className="text-2xl font-semibold mb-4">Koleksi Terbaru</h2>
        <div className="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-4">
          {[
            { name: "Sneakers Pria Casual", price: "Rp 599.000", img: "/api/placeholder/300/200" },
            { name: "Heels Wanita Elegan", price: "Rp 799.000", img: "/api/placeholder/300/200" },
            { name: "Sepatu Lari Performa Tinggi", price: "Rp 1.299.000", img: "/api/placeholder/300/200" },
            { name: "Sandal Anak Nyaman", price: "Rp 299.000", img: "/api/placeholder/300/200" }
          ].map((item, index) => (
            <div key={index} className="border p-4 rounded shadow-md">
              <img src={item.img} alt={item.name} className="w-full h-40 object-cover mb-2 bg-gray-200" />
              <h3 className="font-semibold">{item.name}</h3>
              <p className="text-gray-600">{item.price}</p>
              <button className="mt-2 bg-blue-600 text-white px-4 py-2 rounded w-full hover:bg-blue-700 transition">
                Tambah ke Keranjang
              </button>
            </div>
          ))}
        </div>
      </main>

      <footer className="bg-gray-200 p-4 mt-8">
        <div className="container mx-auto text-center">
          &copy; 2024 ShoesParadise. Semua hak cipta dilindungi.
        </div>
      </footer>
    </div>
  );
}
