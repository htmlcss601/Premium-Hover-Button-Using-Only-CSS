    /* ===== RESET ===== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", sans-serif;
    }

    body {
      height: 100vh;
      background: radial-gradient(circle at top, #111827, #020617);
      display: flex;
      justify-content: center;
      align-items: center;
    }

    /* ===== PREMIUM BUTTON ===== */
    .premium-btn {
      position: relative;
      padding: 18px 56px;
      font-size: 18px;
      font-weight: 500;
      color: #f8fafc;
      background: linear-gradient(
        120deg,
        #1e293b,   /* Midnight Slate */
        #4f46e5,   /* Royal Indigo */
        #6d28d9    /* Deep Purple */
      );
      background-size: 200%;
      border: none;
      border-radius: 999px;
      cursor: pointer;
      overflow: hidden;
      transition:
        transform 0.4s ease,
        box-shadow 0.4s ease,
        background-position 0.6s ease;
    }

    /* Text layer */
    .premium-btn span {
      position: relative;
      z-index: 2;
      letter-spacing: 0.3px;
    }

    /* ===== LIGHT REFLECTION ===== */
    .premium-btn::before {
      content: "";
      position: absolute;
      top: -60%;
      left: -120%;
      width: 60%;
      height: 220%;
      background: rgba(255, 255, 255, 0.15);
      transform: rotate(25deg);
      transition: left 0.8s ease;
      z-index: 1;
    }

    /* ===== SOFT GLOW ===== */
    .premium-btn::after {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(
        120deg,
        rgba(79, 70, 229, 0.5),
        rgba(109, 40, 217, 0.5)
      );
      filter: blur(32px);
      opacity: 0;
      z-index: -1;
      transition: opacity 0.4s ease;
    }

    /* ===== HOVER STATE ===== */
    .premium-btn:hover {
      transform: translateY(-6px);
      box-shadow:
        0 20px 45px rgba(79, 70, 229, 0.35),
        0 10px 25px rgba(109, 40, 217, 0.25);
      background-position: right;
    }

    .premium-btn:hover::before {
      left: 160%;
    }

    .premium-btn:hover::after {
      opacity: 1;
    }

    .premium-btn:active {
      transform: translateY(-2px);
    }
