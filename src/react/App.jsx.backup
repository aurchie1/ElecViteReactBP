import { useState } from "react";

const startingCards = [
  { id: "A-hearts", rank: "A", suit: "♥", color: "red" },
  { id: "7-clubs", rank: "7", suit: "♣", color: "black" },
  { id: "Q-diamonds", rank: "Q", suit: "♦", color: "red" },
  { id: "10-spades", rank: "10", suit: "♠", color: "black" },
  { id: "4-hearts", rank: "4", suit: "♥", color: "red" }
];

export default function App() {
  const [cards, setCards] = useState(startingCards);
  const [message, setMessage] = useState(
    "React is working inside Electron."
  );

  function resetCards() {
    setCards(startingCards);
    setMessage("Cards reset.");
  }

  return (
    <main className="app">
      <header>
        <div>
          <h1>CardForge</h1>
          <p>{message}</p>
        </div>

        <button type="button" onClick={resetCards}>
          Reset cards
        </button>
      </header>

      <section className="table">
        <div className="pile">
          <h2>Discard pile</h2>

          <div className="card card--red">
            <span className="rank">8</span>
            <span className="suit">♥</span>
          </div>
        </div>

        <div className="hand-area">
          <h2>Your hand</h2>

          <div className="hand">
            {cards.map((card) => (
              <button
                key={card.id}
                className={`card card--${card.color}`}
                type="button"
                onClick={() => {
                  setMessage(`You selected ${card.rank}${card.suit}.`);
                }}
              >
                <span className="rank">{card.rank}</span>
                <span className="suit">{card.suit}</span>
              </button>
            ))}
          </div>
        </div>
      </section>
    </main>
  );
}
