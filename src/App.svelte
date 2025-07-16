<script>
  import ImageCard from "./lib/ImageCard.svelte";

  let name = "Aastha Mirchandani";
  let favoriteNumber = 7;
  let bio =
    "I'm a Business Analytics and Computer Science student passionate about real estate, technology, and making education more accessible for everyone.";

  let hobbies = [
    {
      name: "Volunteering",
      icon: "https://images.pexels.com/photos/6646917/pexels-photo-6646917.jpeg",
    },
    {
      name: "Exploring Real Estate",
      icon: "https://images.pexels.com/photos/31821415/pexels-photo-31821415.jpeg",
    },
    {
      name: "Sleeping",
      icon: "https://images.pexels.com/photos/1028741/pexels-photo-1028741.jpeg",
    },
    {
      name: "Painting",
      icon: "https://images.pexels.com/photos/1585325/pexels-photo-1585325.jpeg",
    },
    {
      name: "Hiking",
      icon: "https://images.pexels.com/photos/2398220/pexels-photo-2398220.jpeg",
    },
    {
      name: "Reading about AI",
      icon: "https://images.pexels.com/photos/16380906/pexels-photo-16380906.jpeg",
    },
    {
      name: "Attending conferences",
      icon: "https://images.pexels.com/photos/8761334/pexels-photo-8761334.jpeg",
    },
    {
      name: "Trying new cuisines",
      icon: "https://images.pexels.com/photos/958545/pexels-photo-958545.jpeg",
    },
  ];

  let cardData = [
    {
      image:
        "https://images.pexels.com/photos/4439901/pexels-photo-4439901.jpeg",
      title: "Coding",
      description:
        "I love solving problems and writing code to build cool things.",
    },
    {
      image:
        "https://images.pexels.com/photos/1031588/pexels-photo-1031588.jpeg",
      title: "Reading",
      description: "Books help me grow intellectually and creatively.",
    },
    {
      image:
        "https://images.pexels.com/photos/3278215/pexels-photo-3278215.jpeg",
      title: "Traveling",
      description:
        "I enjoy exploring new cultures and learning from the world around me.",
    },
  ];
</script>

<main>
  <h1>Hello, I'm <span class="highlight">{name}</span>!</h1>
  <p>Favorite number: <strong class="number">{favoriteNumber}</strong></p>
  <p>{bio}</p>

  <h2 class="section-title">Hobbies</h2>
  <ul class="hobby-list">
    {#each hobbies as hobby}
      <li class="hobby-item">
        <img src={hobby.icon} alt={hobby.name} />
        {hobby.name}
      </li>
    {/each}
  </ul>

  <h2 class="section-title">What I Love</h2>
  <div class="card-container">
    {#each cardData as card}
      <div class="card">
        <img src={card.image} alt={card.title} />
        <h3>{card.title}</h3>
        <p>{card.description}</p>
      </div>
    {/each}
  </div>

</main>

<style>
  main {
    margin: 0;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(to right, #f3f0ff, #e8f0ff);
    color: #333;
  }

  main {
    max-width: 900px;
    margin: 3rem auto;
    padding: 2.5rem;
    background-color: #ffffff;
    border-radius: 16px;
    box-shadow: 0 6px 24px rgba(0, 0, 0, 0.08);
  }

  h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    color: #4b3f72;
  }

  .highlight {
    color: #7149c6;
  }

  .number {
    color: #ff7f50;
  }

  p {
    font-size: 1.1rem;
    line-height: 1.6;
    margin-bottom: 1rem;
  }

  .section-title {
    margin-top: 2.5rem;
    font-size: 1.8rem;
    color: #444;
    border-bottom: 2px solid #d1c4e9;
    padding-bottom: 0.5rem;
  }

  .hobby-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 1rem;
    margin-top: 1rem;
    padding: 0;
    list-style: none;
  }

  .hobby-item {
    display: flex;
    align-items: center;
    gap: 0.75rem;
    padding: 0.8rem;
    background-color: #f9f7ff;
    border-radius: 10px;
    border: 1px solid #ddd;
  }

  .hobby-item:hover {
    background-color: #e9e4ff;
  }

  .hobby-item img {
    width: 40px;
    height: 40px;
    border-radius: 8px;
  }

  .card-container {
    display: flex;
    flex-wrap: wrap;
    gap: 1.5rem;
    margin-top: 1.5rem;
  }

  .card {
    flex: 1 1 280px;
    background-color: #fafafa;
    border: 1px solid #dcdcdc;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
    transition: transform 0.2s ease;
  }

  .card:hover {
    transform: scale(1.02);
  }

  .card img {
    width: 100%;
    height: auto;
  }

  .card h3 {
    margin: 0.8rem;
    font-size: 1.2rem;
    color: #4b3f72;
  }

  .card p {
    margin: 0 0.8rem 1rem;
    font-size: 0.95rem;
  }
</style>
