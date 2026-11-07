* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 40px 20px;
  font-family: Arial, sans-serif;
  color: #203047;
  background: #f3f6f8;
}

.page {
  max-width: 1200px;
  margin: 0 auto;
}

.page-header {
  margin-bottom: 28px;
  text-align: center;
}

.page-header h1 {
  margin: 0 0 8px;
  font-size: clamp(2rem, 5vw, 3rem);
}

.page-header p {
  margin: 0;
  color: #627386;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 18px;
}

.gallery-item {
  position: relative;
  min-width: 0;
  height: 240px;
  margin: 0;
  overflow: hidden;
  border-radius: 12px;
  background: #dce5e8;
  box-shadow: 0 6px 18px #20304718;
}

.gallery-item img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.gallery-item:hover img {
  transform: scale(1.05);
}

.gallery-item figcaption {
  position: absolute;
  right: 0;
  bottom: 0;
  left: 0;
  padding: 24px 14px 12px;
  background: linear-gradient(transparent, #10202dcc);
  color: white;
  font-weight: bold;
}

@media (max-width: 500px) {
  body {
    padding: 28px 14px;
  }

  .gallery {
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 12px;
  }

  .gallery-item {
    height: 190px;
  }
}