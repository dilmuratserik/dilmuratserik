- 👋 Hi, I’m @dilmuratserik
- 👀 I’m interested in PHP,python,java,c++ and ant algorithm.
- 🌱 I’m currently learning C++,python,Java
- 💞️ I’m looking to collaborate with all
- 📫 How to reach me dilmuratserikov@gmail.com telegram:sdilmurat
<h1>Hello!</h1>
<!---
dilmuratserik/dilmuratserik is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<div class="yek-app">
  <div class="yek-app__ctrl">
    <button type="button" class="yek-app__toggle yek-app__toggle--preview">
      <i class="fa fa-eye"></i> <!-- fa-edit -->
      <span>Preview</span> <!-- Edit -->
    </button>
  </div>
  <div id="app-themes" class="yek-app__themes">
    <label><input type="radio" class="yek-app__theme" name="app-themes" value="" /><span> Default </span></label>
    <label><input type="radio" class="yek-app__theme" name="app-themes" value="light" checked="checked" /><span> Light </span></label>
    <label><input type="radio" class="yek-app__theme" name="app-themes" value="dark" /><span> Dark </span></label>
    <label><input type="radio" class="yek-app__theme" name="app-themes" value="violet" /><span> Violet </span></label>
  </div>
  <div class="yek-app__preview">
    <div id="profile-container" class="yek-app__profile">
      <div id="profile" class="yek-profile yek-profile--theme_">

        <div class="yek-profile__card">

          <span id="profile-pro" class="yek-profile__pro"></span>

          <img id="profile-pic" class="yek-profile__pic" width="128" height="128" />

          <h3 id="profile-name" class="yek-profile__name"></h3>
          <h6 id="profile-city" class="yek-profile__city"></h6>
          <p id="profile-desc" class="yek-profile__description"></p>

          <div id="profile-buttons" class="yek-profile__buttons"></div>

          <div class="yek-profile__skills">
            <h6 class="yek-profile__skills_title">Skills</h6>
            <ul id="profile-skills" class="yek-profile__skills_items"></ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<script>
  (function() {
    var links = document.querySelectorAll('a[href]');
    links.forEach(function(link) {
      var href = link.getAttribute('href');
      if (href.indexOf('#') !== 0) {
        link.addEventListener('click', function(event) {
          event.preventDefault();
        });
      }
    });
  }());
</script>

<!--
//- All rights reserved &copy; 2021
//- -
//- Created With &heart; by [https://github.com/miko-github]
//- —
//- Design made by Ildiesign [https://dribbble.com/shots/6276930-Profile-Card-UI-Design]
//-  —
//- Powered by T3MPL [https://t3mpl.n4no.com/]
//- -->
<style>
  /* yek-sass (https://github.com/yek-org/yek-sass) */

.yek-app__profile {
  @include yek-flex(column);
  @include yek-width(100vw);
  @include yek-height($min: 100vh);
}

// app
.yek-app {
  & {
    @include yek-size;
    @include yek-aligns;
    @include yek-flex;
  }

  &__ctrl,
  &__themes {
    position: fixed;
    top: 18px;
    left: 18px;
  }
  &__ctrl {
    display: none;
  }
  &__toggle {
    @include --clear-btn;
    padding: 9px;
    border-radius: 9px;
    background: #333;
    color: #cfcfcf;
    cursor: pointer;
    span {
      margin-left: 4px;
    }
    &:hover {
      box-shadow: 0 0 0 9px #ccc;
    }
    &:active {
      transform: scale(0.9);
      box-shadow: none;
    }
  }

  &__themes {
    @include yek-flex(column);
    @include yek-aligns(space-around);
    @include case(title);

    font-size: 1.1rem;
    padding: 6px;
    border-radius: 9px;
    text-align: center;
    background: #222;
    color: #fff;

    label {
      margin: 21px 8px;
      font-size: 1rem;
    }
    label span {
      padding: 9px;
      border-radius: 9px;
      cursor: pointer;
    }

    input {
      display: none;
    }

    input:checked ~ span {
      box-shadow: 0 0 0 2px #c63;
    }
    span:hover {
      box-shadow: 0 0 0 1px #fff;
    }
    span:active {
      box-shadow: 0 0 0 6px #d96;
    }
  }
}
// themes

/* default */
.yek-profile {
  & {
    @include yek-flex(column);
    @include yek-align;
    flex: 1;
  }
  &__name {
    margin: 10px 0;
  }
  &__city {
    @include case(upper);
    margin: 5px 0;
  }
  &__description {
    font-size: 14px;
    line-height: 21px;
  }
  &__card {
    @include yek-width(350px, 100%);
    position: relative;
    padding-top: 30px;
    border-radius: 5px;
    text-align: center;
    box-shadow: 0px 10px 20px -10px rgba(0, 0, 0, 0.75);
  }
  &__pro {
    border-radius: 3px;
    font-size: 14px;
    font-weight: bold;
    padding: 3px 7px;
    position: absolute;
    top: 30px;
    left: 30px;
  }
  &__pic {
    border: 1px solid #000;
    border-radius: 50%;
    padding: 7px;
  }

  &__button {
    display: inline-block;
    margin: 5px;
    padding: 10px 25px;
    border: 1px solid #000;
    border-radius: 3px;
    font-family: Montserrat, sans-serif;
    font-weight: 500;
    text-decoration: none;
    &:hover {
      opacity: 0.5;
    }
    &:not(&--primary) {
      background-color: transparent !important;
    }
  }

  &__skills {
    padding: 12px 6px;
    margin-top: 30px;
    text-align: left;
  }
  &__skills_title {
    @include case(upper);
    padding: 0 7px;
    margin: 18px 0;
  }
  &__skills_items {
    @include --clear-list;
  }
  &__skills_item {
    display: inline-block;
    border: 1px solid #000;
    border-radius: 3px;
    margin: 0 5px 5px;
    padding: 7px;
    font-size: 12px;
  }
}

/* violet */
.yek-profile {
  &--theme_violet {
    background-color: #28223f;
  }
  &--theme_violet &__card {
    background-color: #231e39; // same-1
    color: #b3b8cd;
  }
  &--theme_violet &__pic {
    border-color: #03bfcb; // same-2
  }
  &--theme_violet &__pro {
    color: #231e39; // same-1
    background-color: #febb0b;
  }
  &--theme_violet &__button {
    &--primary {
      background-color: #03bfcb; // same-2
      color: #231e39; // same-1
    }
    border-color: #03bfcb; // same-2
    color: #02899c;
  }
  &--theme_violet &__skills {
    background: #1f1a36;
  }
  &--theme_violet &__skills_item {
    border-color: #2d2747;
  }
}

/* dark */
.yek-profile {
  &--theme_dark {
    background-color: #1c1c1c;
  }
  &--theme_dark &__card {
    background-color: #313131;
    color: #d3d3d3;
  }
  &--theme_dark &__pic {
    border-color: #d3d3d3;
  }
  &--theme_dark &__pro {
    color: #1c1c1c;
    background: #fff;
  }
  &--theme_dark &__button {
    &--primary {
      background-color: #febb0b;
      color: #1c1c1c;
    }
    border-color: #febb0b;
    color: #febb0b;
  }
  &--theme_dark &__skills {
    background: #1c1c1c;
  }
  &--theme_dark &__skills_item {
    border-color: #343434;
  }
}

/* light */

.yek-profile {
  &--theme_light {
    background-color: #cecece;
  }
  &--theme_light &__card {
    background-color: #fff;
    color: #313131;
  }
  &--theme_light &__pic {
    border-color: #d3d3d3;
  }
  &--theme_light &__pro {
    color: #fff;
    background: #1c1c1c;
  }
  &--theme_light &__button {
    &--primary {
      background-color: #febb0b;
      border-color: #febb0b;
      color: #1c1c1c;
    }
    border-color: #d3d3d3;
    color: #313131;
  }
  &--theme_light &__skills {
    background: #1c1c1c;
    color: #a0a0a0;
  }
  &--theme_light &__skills_item {
    border-color: #343434;
  }
}

// &--theme_violet &__footer {
// 	background: #222;
// 	color: #fff;
// 	a {
// 		color: #3c97bf;
// 	}
// }
// &--theme_dark &__footer {
// 	background: #080808;
// 	color: #747474;
// 	a {
// 		color: #939393;
// 	}
// }
// &--theme_light footer {
// 	background: transparent;
// 	color: #747474;
// 	a {
// 		color: #747474;
// 	}
// }
<script>
  // powered by https://miko-github.github.io/miko-github //

// GENERATORS //

function $btns(buttons) {
  return buttons.map(({ href, label, primary }) => {
    let _attrs = {
      href,
      target: "__blank",
      class: `yek-profile__button ${
        primary ? "yek-profile__button--primary" : ""
      }`
    };
    return createElement("a", _attrs, label);
  });
}
function $skills(skills) {
  return skills.map((skill) => {
    let _attrs = { class: "yek-profile__skills_item" };
    return createElement("li", _attrs, skill);
  });
}

function generateCard({
  badge,
  avatar,
  name,
  city,
  description: desc,
  buttons,
  skills
}) {
  // selectors
  const $_pro = query("#profile-pro");
  const $_pic = query("#profile-pic");
  const $_name = query("#profile-name");
  const $_city = query("#profile-city");
  const $_desc = query("#profile-desc");
  const $_btns = query("#profile-buttons");
  const $_skills = query("#profile-skills");

  // appends
  append($_pro, badge);
  $_pic.setAttribute("src", avatar);
  $_pic.setAttribute("alt", name);
  append($_name, name);
  append($_city, city);
  append($_desc, desc);
  append($_btns, $btns(buttons));
  append($_skills, $skills(skills));
}

function $meta(data) {
  let _data = _.map(data, (value, key) => ({ key, value }));
  let $_meta = createElement("meta", null, null);
  _data.map(({ key, value }) => {
    $_meta.setAttribute(key, value);
  });
  return $_meta;
}

function $theme($_element, theme) {
  let regex = /--theme_([\w\s\d]{0,})$/gi;
  $_element.className = $_element.className.replace(regex, `--theme_${theme}`);
}

function generateMeta({
  theme,
  title,
  favicon,
  description: desc,
  ogImage: og
}) {
  const $_head = document.head;
  const $_profile = document.querySelector("#profile");
  $theme($_profile, theme);

  document.title = title;
  append($_head, createElement("link", { rel: "icon", href: favicon }, null));
  append($_head, $meta({ name: "description", content: desc }));
  append($_head, $meta({ property: "og:title", content: title }));
  append($_head, $meta({ property: "og:description", content: desc }));
  append($_head, $meta({ property: "og:image", content: og }));
}

function generate({ metadata, body }) {
  generateCard(body);
  generateMeta(metadata);
}

// GENERATE //

const __image = `https://raw.githubusercontent.com/miko-github/miko-github/gh_page/assets/image.png`;
const dataset = {
  metadata: {
    theme: "light", // light | dark | violet | ''
    title: "Mikoloism - Fullstack Developer",
    description: "Mikoloism - Fullstack Developer",
    favicon: __image,
    ogImage: __image
  },
  body: {
    badge: "Dev",
    avatar: __image,
    name: "Miko Mikoloism",
    city: "Iran",
    description: "Fullstack Developer",
    buttons: [
      {
        primary: false,
        label: "Codepen",
        href: "https://codepen.io/miko-github"
      },
      { primary: true, label: "GitHub", href: "https://github.com/miko-github" }
    ],
    skills: [
      "Javascript",
      "Typescript",
      "ReactJS",
      "Vue",
      "ExpressJS",
      "ElectronJS",
      "Ionic Framework",
      "HTML / CSS",
      "PostgreSQL",
      "Sass / SCSS",
      "Bootstrap",
      "MySQL",
      "MongoDB / Mongoose"
    ]
  }
};

generate(dataset);

// theme-select //

const $_theme = document.querySelector("#app-themes");
$_theme.onchange = function ({ target: { value } }) {
  // dataset.metadata.theme = value;
  $theme(document.querySelector("#profile"), value);
};

  </script>
  </style>
