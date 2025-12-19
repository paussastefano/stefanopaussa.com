# Stefano Paussa Portfolio

Portfolio website for Stefano Paussa - Videographer and Editor based in Milano.

## Project Structure

```
/
├── index.html              # Landing page with video
├── home.html              # Main home page with navigation
├── works.html             # Projects grid with filters
├── work-detail.html       # Single project detail page
├── about.html             # About/Contact page
├── css/
│   └── style.css          # Main stylesheet
├── fonts/
│   ├── AlteHaasGroteskRegular.ttf
│   └── AlteHaasGroteskBold.ttf
├── images/
│   ├── projects/          # Project thumbnails and images
│   └── photography/       # Photography project images
└── data/
    └── projects.json      # All project data
```

## How to Add a New Project

1. **Add project images:**
   - For editing/videography projects: Add thumbnail to `/images/projects/`
   - For photography projects: Add images to `/images/photography/`

2. **Edit `data/projects.json`:**
   Add a new object to the array with the following structure:

```json
{
  "id": "unique-project-id",
  "title": "Project Title",
  "role": "Your Role (e.g., Editor, Director, Photographer)",
  "category": "editing|videography|photography",
  "thumbnail": "images/projects/your-thumbnail.jpg",
  "videoUrl": "https://www.youtube.com/embed/VIDEO_ID",
  "description": "Project description text",
  "credits": [
    { "role": "Director", "name": "Name Surname" },
    { "role": "Editor", "name": "Stefano Paussa" },
    { "role": "DOP", "name": "Name Surname" }
  ]
}
```

3. **Field explanations:**
   - `id`: Unique identifier (use lowercase with hyphens, e.g., "project-name-2024")
   - `title`: Project name shown on the site
   - `role`: Stefano's role in this project
   - `category`: Must be one of: `editing`, `videography`, or `photography`
   - `thumbnail`: Path to thumbnail image (relative to site root)
   - `videoUrl`: YouTube embed URL (leave empty `""` for photography projects without video)
   - `description`: Brief project description
   - `credits`: Array of people involved (role and name)

4. **Save the file** - changes will appear immediately when you refresh the site

## Categories

- **Editing**: Projects where Stefano worked primarily as an editor
- **Videography**: Projects involving filming/direction
- **Photography**: Still photography work

## Local Development

Simply open `index.html` in a web browser to view the site locally.

For production deployment on GitHub Pages, the site will be available at:
`https://paussastefano.github.io/stefanopaussa.com/`

## Next Steps (Hugo + Decap CMS)

This current setup uses JSON + JavaScript for content management.
Future migration to Hugo + Decap CMS will provide:
- Static site generation
- Visual content management interface
- Better performance
- Easier content updates without editing JSON manually
