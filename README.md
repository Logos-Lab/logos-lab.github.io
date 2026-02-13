# Logos Robotics Lab Website

**Logos** is a robotics laboratory headed by Prof. Nakul Gopalan at Arizona State University. Our lab works on Language Grounding, Task and Motion Planning, and Robot Learning problems.

The website is created using a template from [Allan Lab](https://www.allanlab.org/)!

---

## Table of Contents

1. [Getting Started (Clone & Run Locally)](#getting-started-clone--run-locally)
2. [Git Workflow (Branches & Pull Requests)](#git-workflow-branches--pull-requests)
3. [Updating Your Profile (Masters & PhD Students)](#updating-your-profile-masters--phd-students)
4. [Adding a New Publication](#adding-a-new-publication)
5. [Adding a News Item](#adding-a-news-item)

---

## Getting Started (Clone & Run Locally)

### Prerequisites

- **Git** — [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- **Ruby** (>= 2.5) and **Bundler** — [Install Ruby](https://www.ruby-lang.org/en/documentation/installation/)
- **Jekyll** — installed automatically via Bundler (see below)

### 1. Clone the Repository

```bash
git clone https://github.com/Logos-Lab/logos-lab.github.io.git
cd logos-lab.github.io
```

### 2. Install Dependencies

```bash
gem install bundler   # if you don't have bundler already
bundle install
```

### 3. Run the Site Locally

```bash
bundle exec jekyll serve
```

The site will be available at **http://localhost:4000**. Changes to most files will auto-reload; if you edit `_config.yml`, you need to restart the server.

---

## Git Workflow (Branches & Pull Requests)

> **⚠️ IMPORTANT: Do NOT commit directly to `gh-pages`.** All changes must go through a pull request.

1. **Create a new branch** for your changes:

   ```bash
   git checkout gh-pages
   git pull origin gh-pages          # make sure you're up to date
   git checkout -b <your-branch>     # e.g. git checkout -b update-omkar-profile
   ```

2. **Make your changes** (edit files, add images, etc.).

3. **Commit and push** your branch:

   ```bash
   git add .
   git commit -m "Brief description of your change"
   git push origin <your-branch>
   ```

4. **Open a Pull Request** on GitHub:
   - Go to the repository on GitHub: https://github.com/Logos-Lab/logos-lab.github.io
   - Click **"Compare & pull request"** for your branch.
   - Set the base branch to **`gh-pages`**.
   - Add a short description and request a review.

5. **Once approved and merged**, your changes will be live on the website.

---

## Updating Your Profile (Masters & PhD Students)

Student profiles are stored in YAML files inside the `_data/` directory, and photos are stored in `images/teampic/`.

- **PhD students** → edit `_data/team_members.yml`
- **Masters students** → edit `_data/students.yml`

### Profile Fields

Each entry in the YAML file looks like this:

```yaml
- name: Your Full Name
  website: https://your-website.com/
  photo: your_photo.jpg
  info: PhD Student          # or "Masters Student"
  joined: Fall 2024          # semester you joined
```

| Field     | Description                                                                 |
| --------- | --------------------------------------------------------------------------- |
| `name`    | Your full name as you want it displayed.                                    |
| `website` | URL to your personal website, LinkedIn, Google Scholar, etc.                |
| `photo`   | Filename of your photo in `images/teampic/` (see below).                   |
| `info`    | Your role, e.g. `PhD Student`, `Masters Student`.                          |
| `joined`  | The semester you joined, e.g. `Fall 2024`.                                 |

### Adding or Updating Your Photo

1. Add your photo to the `images/teampic/` directory.
   - Use a **square** image (e.g. 300×300 px) for best results.
   - Use a descriptive filename (e.g. `firstname_lastname.jpg`).
2. Update the `photo` field in your YAML entry to match the filename.

### Example: Updating an Existing Entry

If your current entry in `_data/team_members.yml` is:

```yaml
- name: Omkar Patil
  website: https://omkarpatil18.github.io/
  photo: s2.jpg
  info: PhD Student
  joined: Fall 2023
```

And you want to update your photo and website, change it to:

```yaml
- name: Omkar Patil
  website: https://my-new-website.com/
  photo: omkar_patil.jpg
  info: PhD Student
  joined: Fall 2023
```

Then place `omkar_patil.jpg` in the `images/teampic/` folder.

### Example: Adding a New Entry

Add a new block at the end of the appropriate file (`team_members.yml` for PhD, `students.yml` for Masters):

```yaml
- name: Jane Doe
  website: https://janedoe.com/
  photo: jane_doe.jpg
  info: Masters Student
  joined: Spring 2026
```

---

## Adding a New Publication

Publications are listed in `_data/publist.yml`. Publication images go in `images/pubpic/`.

### Publication Fields

```yaml
- title: "Your Paper Title"
  image: your_paper_figure.png
  description: "A brief description of the paper (1–3 sentences)."
  authors: Author One, Author Two, Author Three
  link:
    url: https://arxiv.org/abs/XXXX.XXXXX
    display: "2026 IEEE International Conference on Robotics and Automation (ICRA)"
  highlight: 1
```

| Field         | Description                                                                                  |
| ------------- | -------------------------------------------------------------------------------------------- |
| `title`       | The full title of the paper.                                                                 |
| `image`       | Filename of a figure/thumbnail in `images/pubpic/`. Use a representative figure from the paper. |
| `description` | A short summary (1–3 sentences) of the paper.                                                |
| `authors`     | Comma-separated list of authors.                                                             |
| `link.url`    | URL to the paper (arXiv, IEEE, conference page, etc.).                                       |
| `link.display`| Venue name and year (e.g. `ICRA 2026`, `IROS 2025`).                                       |
| `highlight`   | Set to `1` to feature the paper prominently on the homepage, `0` otherwise.                  |

### Steps

1. **Add your paper image** to `images/pubpic/` (a clear figure or diagram from the paper).
2. **Add a new entry** at the **top** of `_data/publist.yml` (newest publications should come first):

   ```yaml
   - title: "My Awesome Paper Title"
     image: my_paper_fig.png
     description: "We propose a novel method for ..."
     authors: Alice, Bob, Charlie
     link:
       url: https://arxiv.org/abs/XXXX.XXXXX
       display: "ICRA 2026"
     highlight: 1
   ```

3. Follow the [Git Workflow](#git-workflow-branches--pull-requests) to submit a PR.

---

## Adding a News Item

News items are listed in `_data/news.yml` and appear on the homepage.

### News Fields

```yaml
- date: 1 January 2026
  headline: "Your news headline here. You can use [Markdown links](https://example.com)."
```

| Field      | Description                                                                          |
| ---------- | ------------------------------------------------------------------------------------ |
| `date`     | The date of the news item (e.g. `Jan 1 2026`, `15 December 2025`).                  |
| `headline` | A short description. Supports Markdown-style links: `[text](url)`.                  |

### Steps

1. Open `_data/news.yml`.
2. Add a new entry at the **top** of the file (newest first):

   ```yaml
   - date: Feb 12 2026
     headline: "Our paper on [Cool Robots](https://arxiv.org/abs/XXXX.XXXXX) has been accepted to ICRA 2026!"
   ```

3. Follow the [Git Workflow](#git-workflow-branches--pull-requests) to submit a PR.

---

## Questions?

If you run into issues with the website, reach out to the lab members or open an issue on the [GitHub repository](https://github.com/Logos-Lab/logos-lab.github.io/issues).
