# 🚀 VASU SHARMA - 3D Interactive Portfolio


Welcome to my personal portfolio website! 🎉 This project showcases my journey as an **AI Enthusiast** and **Computer Science Engineer** with 1.5 years of experience in Development, DevOps & Database management. Built with cutting-edge web technologies, this portfolio demonstrates my skills through stunning 3D animations and interactive experiences.

### 🌐 Live Preview: [https://portfolio-vasusharma.netlify.app](https://portfolio-vasusharma.netlify.app)
                      [vasusharma.vercel.app](vasusharma.vercel.app)

## 👨‍💻 About Me

I'm **VASU SHARMA**, a Computer Science Engineer with hands-on experience in:
- **Development**: Full-stack web development with modern frameworks
- **DevOps & DevSecOps**: Deploying and automating workflows
- **Database Management**: Designing and optimizing database systems
- **AI & AIOps**: Solving real-life problems with artificial intelligence
- **Cloud Technologies**: AWS and Azure
- **International Collaboration**: Working with foreign clients

I bring strong analytical skills, effective communication, and a team-oriented approach to driving process improvements and delivering results.

## 🔥 Features

### 🎹 **3D Interactive Animations**
- Custom-made interactive keyboard built with **Spline**
- Each keycap represents a skill and reveals details on hover
- Smooth, responsive 3D interactions that captivate visitors

### ✨ **Slick Interactions & Animations**
- Powered by **GSAP** and **Framer Motion**
- Buttery-smooth animations on scroll, hover, and element reveals
- Creative motion designs that enhance storytelling

### 🌌 **Space-Themed Design**
- Particles floating on a dark, cosmic background
- Unique and futuristic aesthetic
- Immersive user experience

### 📱 **Fully Responsive**
- Optimized for all devices (desktop, tablet, mobile)
- Beautiful design that scales seamlessly
- Touch-friendly interactions

### 🎨 **Modern UI Components**
- Built with **Shadcn UI** and **Aceternity UI**
- Accessible and customizable components
- Consistent design system throughout

## 🛠️ Tech Stack

### Frontend
- **Framework**: Next.js 14.2.3
- **UI Library**: React 18
- **Styling**: Tailwind CSS, Shadcn UI, Aceternity UI
- **Animations**: GSAP, Framer Motion, Spline Runtime
- **3D Graphics**: Three.js, Spline

### Backend & Services
- **Email Service**: Resend
- **Real-time Communication**: Socket.io
- **Validation**: Zod

### Development Tools
- **Language**: TypeScript
- **Linting**: ESLint
- **Package Manager**: npm

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ installed
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/vasudevsharmalive-code/3D-interactive-portfolio.git
   ```

2. **Navigate to the project directory**
   ```bash
   cd 3D-interactive-portfolio
   ```

3. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

4. **Set up environment variables**
   
   Create a `.env.local` file in the root directory:
   ```bash
   # Copy the example file
   cp .env.example .env.local
   ```
   
   Add your Resend API key:
   ```env
   RESEND_API_KEY=your_resend_api_key_here
   ```
   
   Get your API key from [Resend](https://resend.com)

5. **Start the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

6. **Open your browser**
   
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📦 Build for Production

```bash
npm run build
npm start
```

## 🌐 Deployment

### Deploy to Vercel (Recommended)

This project is optimized for **Vercel** deployment:

1. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Ready for deployment"
   git push origin main
   ```

2. **Deploy to Vercel**
   - Visit [vercel.com](https://vercel.com)
   - Import your GitHub repository
   - Vercel will auto-detect Next.js settings
   - Add environment variables:
     - `RESEND_API_KEY`: Your Resend API key

3. **Automatic Deployments**
   - Every push to `main` triggers a new deployment
   - Preview deployments for pull requests
   - Instant rollbacks if needed

### Environment Variables on Vercel

1. Go to your Vercel project dashboard
2. Navigate to **Settings** → **Environment Variables**
3. Add the following variables:
   - **RESEND_API_KEY**: Your Resend API key from [resend.com](https://resend.com)
4. Redeploy the application

### Alternative Deployment Options

This portfolio can also be deployed to:
- **Netlify**: Connect your GitHub repo
- **AWS Amplify**: Use the AWS Console
- **Railway**: One-click deployment
- **Self-hosted**: Use Docker or traditional hosting

## 📁 Project Structure

```
3D-interactive-portfolio/
├── public/              # Static assets
│   └── assets/         # Images, icons, SEO files
├── src/
│   ├── app/            # Next.js app directory
│   ├── components/     # React components
│   │   ├── header/    # Header configuration
│   │   ├── footer/    # Footer configuration
│   │   └── ui/        # UI components
│   └── data/          # Configuration and data
│       ├── config.ts  # Site configuration
│       └── projects.tsx # Projects data
├── .env.example       # Environment variables template
├── .gitignore         # Git ignore rules
├── vercel.json        # Vercel configuration
├── next.config.mjs    # Next.js configuration
├── tailwind.config.ts # Tailwind CSS configuration
└── package.json       # Dependencies
```

## 🎯 Key Files

- **`src/data/config.ts`**: Site metadata, SEO, social links
- **`src/data/projects.tsx`**: Portfolio projects showcase
- **`src/components/header/config.ts`**: Navigation configuration
- **`src/components/footer/config.ts`**: Footer links and info

## 🔧 Configuration

### Update Site Information

Edit `src/data/config.ts`:
```typescript
const config = {
  title: "Your Name | Your Title",
  description: { /* ... */ },
  author: "Your Name",
  email: "your.email@example.com",
  site: "https://yourwebsite.com",
  // ...
}
```

### Add Projects

Edit `src/data/projects.tsx`:
```typescript
const projects: Project[] = [
  {
    id: "project-1",
    title: "Project Name",
    category: "Web Development",
    // ... more fields
  }
]
```

## 📝 Available Scripts

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm start        # Start production server
npm run lint     # Run ESLint
```

## 🎨 Customization

### Styling
- Modify `tailwind.config.ts` for design tokens
- Edit component styles in respective files
- Update theme colors and spacing

### Animations
- GSAP timeline animations in components
- Framer Motion variants for micro-interactions
- Spline 3D scene configurations

### Content
- Update personal info in `src/data/config.ts`
- Add projects in `src/data/projects.tsx`
- Modify navigation in header config

## 🐛 Troubleshooting

### Build Errors
- Clear `.next` folder: `rm -rf .next`
- Delete `node_modules` and reinstall: `rm -rf node_modules && npm install`
- Check Node.js version (18+ required)

### Environment Variables
- Ensure `.env.local` exists
- Verify variable names match code
- Restart dev server after changes

### Animation Issues
- Check browser compatibility
- Ensure GSAP/Framer Motion loaded
- Verify 3D model file paths

## 🤝 Contributing

While this is a personal portfolio, suggestions and improvements are welcome!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is open source and available for personal and educational use. Please provide attribution if you use significant portions of the code.

## 🙏 Acknowledgments

This project is **inspired** by the amazing work of:
- [Naresh Khatri](https://github.com/Naresh-Khatri/Portfolio) - Innovative web design approach
- [Abhijit Zende](https://github.com/Abhiz2411/3D-interactive-portfolio) - Original template creator

Thank you for the inspiration! 💡

## 📬 Contact Me

Let's connect! I'm always open to collaboration, feedback, or just a friendly chat:

- **Email**: [heyits.vasudevsharma@gmail.com](mailto:heyits.vasudevsharma@gmail.com)
- **GitHub**: [@vasudevsharmalive-code](https://github.com/vasudevsharmalive-code)
- **CodePen**: [@mustbevasudev](https://codepen.io/mustbevasudev)
- **Website**: [vasusharma.com](https://vasusharma.com)

## 💼 Hire Me

I'm available for:
- Full-stack development projects
- DevOps and cloud infrastructure
- AI/ML integration
- Database design and optimization
- Technical consulting

Feel free to reach out for opportunities!

---

### ⭐ Star This Repo!

If you find this project helpful or inspiring, please give it a star! It helps others discover this work.

**Made with ❤️ by VASU SHARMA**
