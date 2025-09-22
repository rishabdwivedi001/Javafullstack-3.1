// src/components/ProductCard.jsx
import React from "react";

function ProductCard({ name, price, inStock }) {
  const statusText = inStock ? "In Stock" : "Out of Stock";
  const statusColor = inStock ? "#0f766e" : "#b91c1c";

  return (
    <div style={styles.card}>
      <h3 style={styles.title}>{name}</h3>
      <p style={styles.text}>Price: ${price}</p>
      <p style={{ ...styles.text, color: statusColor }}>Status: {statusText}</p>
    </div>
  );
}

const styles = {
  card: {
    border: "1px solid #e5e7eb",
    borderRadius: 12,
    padding: 16,
    width: 260,
    boxShadow: "0 2px 10px rgba(0,0,0,0.06)",
    background: "#fff",
    textAlign: "center",
  },
  title: { margin: "4px 0 8px", fontSize: 20 },
  text: { margin: "6px 0", fontSize: 16 },
};

export default ProductCard;
