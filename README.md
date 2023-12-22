# Guidance to Run the Project

### In First Terminal
cd website_for_mike/api
pip install -r requirements.txt
<run the file api.py>

### In Second Terminal
cd website_for_mike
npm install
export NODE_OPTIONS=--openssl-legacy-provider
npm start



### frontend
export NODE_OPTIONS=--openssl-legacy-provider
npm install @mui/material @emotion/react @emotion/styled
npm install @mui/icons-material
npm install react-treebeard
npm install @mui/x-data-grid
npm install react-markdown
npm install react-pro-sidebar
npm install lodash


### backend
flask run
npx create-react-app frontend
pip install SQLAlchemy Flask-SQLAlchemy
npm install http-proxy-middleware --save
pip install Flask-Migrate
pip install markdown
npm install axios 


### database
sqlite3 blog_database.db
.tables     <!-- return ... -->
.schema ...
SELECT * FROM ...
.exit


CREATE TABLE Posts (
    post_id INTEGER PRIMARY KEY,
    title TEXT,
    content TEXT,
    number_of_views INTEGER
);

CREATE TABLE Tags (
    tag_id INTEGER PRIMARY KEY,
    tag_name TEXT
);

CREATE TABLE PostTags (
    post_id INTEGER,
    tag_id INTEGER,
    PRIMARY KEY (post_id, tag_id),
    FOREIGN KEY (post_id) REFERENCES Posts(post_id),
    FOREIGN KEY (tag_id) REFERENCES Tags(tag_id)
);

CREATE TABLE SearchHistory (
    search_id INTEGER PRIMARY KEY,
    search_query TEXT,
    timestamp DATETIME
);

