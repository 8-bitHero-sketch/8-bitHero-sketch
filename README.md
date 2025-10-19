import React, { useState } from 'react';
import { CheckCircle, Circle, ArrowRight, Star } from 'lucide-react';

export default function CareerGapMap() {
  const [selectedCategory, setSelectedCategory] = useState(null);

  const categories = {
    current: {
      title: "✅ What You Already Have",
      color: "bg-green-100 border-green-400",
      items: [
        { name: "Java (CSN Backend Program)", status: "strong", details: "MATCHES: 'foundational knowledge of Java' ✓" },
        { name: "Git/GitHub", status: "learning", details: "PREFERRED SKILL: Keep building GitHub portfolio" },
        { name: "Problem-Solving Skills", status: "strong", details: "Manufacturing troubleshooting = debugging mindset" },
        { name: "Team Collaboration", status: "strong", details: "3+ years leading teams of 7 - they want 'collaborative team environment'" },
        { name: "Communication Skills", status: "strong", details: "Customer service + training experience" },
        { name: "Willingness to Learn", status: "strong", details: "Career pivot shows drive & curiosity" },
        { name: "Process Documentation", status: "strong", details: "SOPs = 'well-documented code'" }
      ]
    },
    marmonNeeds: {
      title: "🎯 What They're Looking For",
      color: "bg-blue-100 border-blue-400",
      items: [
        { name: "Web Development", priority: "required", details: "HTML, CSS, JavaScript - LEARN THESE" },
        { name: "One Programming Language", priority: "required", details: "Java ✓ You have this!" },
        { name: "Version Control (Git)", priority: "preferred", details: "You're learning - expand your GitHub" },
        { name: "Code Reviews", priority: "medium", details: "Participate in peer review process" },
        { name: "Full SDLC Exposure", priority: "high", details: "Concept → deployment understanding" },
        { name: "EdTech Interest", priority: "preferred", details: "Passion for education technology" },
        { name: "AI Tools (Claude!)", priority: "preferred", details: "Familiarity with Claude for coding - YOU'RE USING IT NOW!" }
      ]
    },
    criticalGaps: {
      title: "🚨 MUST-LEARN Before Applying",
      color: "bg-red-100 border-red-400",
      items: [
        { name: "Web Dev Fundamentals", urgency: "immediate", action: "HTML + CSS + JavaScript basics (2 weeks)" },
        { name: "Spring Boot Framework", urgency: "immediate", action: "PREFERRED SKILL - Java backend framework" },
        { name: "Portfolio Projects", urgency: "immediate", action: "2-3 projects showing web apps" },
        { name: "Testing & Debugging", urgency: "high", action: "Learn JUnit, practice debugging in Eclipse" },
        { name: "Basic Database Knowledge", urgency: "high", action: "SQL for web app data storage" }
      ]
    },
    bonusSkills: {
      title: "🌟 Bonus Points (Preferred Skills)",
      color: "bg-purple-100 border-purple-400",
      items: [
        { name: "Spring Boot", impact: "high", details: "Backend framework - Java-based, learn this!" },
        { name: "React", impact: "medium", details: "Front-end framework - they mention it specifically" },
        { name: "Claude AI Tool", impact: "medium", details: "You're literally using it right now - mention this!" },
        { name: "Node.js", impact: "low", details: "Alternative backend - focus on Spring Boot first" },
        { name: "Git/GitHub", impact: "high", details: "You have Git - polish your GitHub profile" }
      ]
    },
    quickWins: {
      title: "⚡ Quick Wins (Next 3 Weeks)",
      color: "bg-yellow-100 border-yellow-400",
      items: [
        { name: "HTML/CSS/JS Crash Course", time: "1 week", details: "FreeCodeCamp or Codecademy - 2 hrs/day" },
        { name: "Spring Boot Tutorial", time: "1 week", details: "Build simple REST API following tutorial" },
        { name: "EdTech Research", time: "2 days", details: "Study World Book products, write cover letter angle" },
        { name: "GitHub Portfolio Polish", time: "2 days", details: "README files, pin best repos, add descriptions" },
        { name: "Practice with Claude", time: "ongoing", details: "Use Claude for coding help - it's a preferred skill!" }
      ]
    },
    projectIdeas: {
      title: "💼 Portfolio Project Ideas",
      color: "bg-indigo-100 border-indigo-400",
      items: [
        { name: "Digital Library Platform", difficulty: "Perfect!", details: "Books, search, user accounts - DIRECTLY relevant to World Book!" },
        { name: "Quiz/Study Tool Web App", difficulty: "Ideal", details: "EdTech connection - students, questions, scoring" },
        { name: "Reading Progress Tracker", difficulty: "Good", details: "Web app for tracking books read - HTML/CSS/JS + Java backend" },
        { name: "Educational Resource Manager", difficulty: "Great", details: "Teachers manage resources - shows EdTech interest" }
      ]
    }
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-blue-50 via-purple-50 to-pink-50 p-8">
      <div className="max-w-7xl mx-auto">
        <div className="text-center mb-8">
          <h1 className="text-4xl font-bold text-slate-800 mb-2">
            Your Path to World Book Software Dev Intern
          </h1>
          <p className="text-slate-600 text-lg mb-1">
            Marmon Holdings (Berkshire Hathaway) • EdTech • $27/hr
          </p>
          <p className="text-sm text-slate-500">
            Remote OR Hybrid (Chicago) • Expected Graduation: 2027 • Target: Apply in 3-4 Weeks
          </p>
        </div>

        <div className="mb-8 bg-gradient-to-r from-blue-500 to-purple-600 text-white rounded-lg p-6 shadow-lg">
          <h2 className="text-2xl font-bold mb-3 flex items-center">
            <Star className="mr-2" />
            KEY INSIGHT: You're a Better Match Than You Think!
          </h2>
          <div className="grid md:grid-cols-2 gap-4 text-sm">
            <div className="bg-white bg-opacity-20 rounded p-3">
              <p className="font-semibold mb-1">✓ They want "willingness to learn" - You're career-pivoting!</p>
            </div>
            <div className="bg-white bg-opacity-20 rounded p-3">
              <p className="font-semibold mb-1">✓ They want "collaborative team environment" - You led teams of 7!</p>
            </div>
            <div className="bg-white bg-opacity-20 rounded p-3">
              <p className="font-semibold mb-1">✓ They want "Claude AI familiarity" - You're using it NOW!</p>
            </div>
            <div className="bg-white bg-opacity-20 rounded p-3">
              <p className="font-semibold mb-1">✓ They want "problem-solving" - You troubleshot equipment & processes!</p>
            </div>
          </div>
        </div>

        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-8">
          {Object.entries(categories).map(([key, category]) => (
            <div
              key={key}
              className={`${category.color} border-2 rounded-lg p-6 cursor-pointer transform transition-all hover:scale-105 hover:shadow-lg ${
                selectedCategory === key ? 'ring-4 ring-blue-400' : ''
              }`}
              onClick={() => setSelectedCategory(selectedCategory === key ? null : key)}
            >
              <h3 className="text-xl font-bold mb-4 text-slate-800">
                {category.title}
              </h3>
              <div className="space-y-3">
                {category.items.map((item, idx) => (
                  <div key={idx} className="bg-white rounded p-3 shadow-sm">
                    <div className="flex items-start justify-between mb-1">
                      <span className="font-semibold text-slate-700 text-sm">
                        {item.name}
                      </span>
                      {item.status && (
                        <span className={`text-xs px-2 py-1 rounded ${
                          item.status === 'strong' ? 'bg-green-200 text-green-800' : 'bg-blue-200 text-blue-800'
                        }`}>
                          {item.status}
                        </span>
                      )}
                      {item.priority && (
                        <span className={`text-xs px-2 py-1 rounded ${
                          item.priority === 'required' ? 'bg-red-200 text-red-800' : 
                          item.priority === 'preferred' ? 'bg-purple-200 text-purple-800' :
                          item.priority === 'high' ? 'bg-orange-200 text-orange-800' :
                          'bg-yellow-200 text-yellow-800'
                        }`}>
                          {item.priority}
                        </span>
                      )}
                      {item.urgency && (
                        <span className={`text-xs px-2 py-1 rounded ${
                          item.urgency === 'immediate' ? 'bg-red-200 text-red-800' : 'bg-orange-200 text-orange-800'
                        }`}>
                          {item.urgency}
                        </span>
                      )}
                      {item.time && (
                        <span className="text-xs px-2 py-1 rounded bg-blue-200 text-blue-800">
                          {item.time}
                        </span>
                      )}
                      {item.difficulty && (
                        <span className="text-xs px-2 py-1 rounded bg-purple-200 text-purple-800">
                          {item.difficulty}
                        </span>
                      )}
                      {item.impact && (
                        <span className={`text-xs px-2 py-1 rounded ${
                          item.impact === 'high' ? 'bg-green-200 text-green-800' : 
                          item.impact === 'medium' ? 'bg-yellow-200 text-yellow-800' :
                          'bg-gray-200 text-gray-800'
                        }`}>
                          {item.impact}
                        </span>
                      )}
                    </div>
                    {selectedCategory === key && (
                      <p className="text-xs text-slate-600 mt-2">
                        {item.details || item.action}
                      </p>
                    )}
                  </div>
                ))}
              </div>
            </div>
          ))}
        </div>

        <div className="bg-white rounded-lg shadow-lg p-8 border-2 border-slate-200 mb-8">
          <h2 className="text-2xl font-bold text-slate-800 mb-6 flex items-center">
            <ArrowRight className="mr-3 text-blue-600" />
            Your 3-Week Sprint to Apply
          </h2>
          
          <div className="space-y-6">
            <div className="border-l-4 border-red-500 pl-6 py-2">
              <h3 className="font-bold text-lg text-red-700 mb-2">Week 1: Web Fundamentals</h3>
              <ul className="space-y-2 text-slate-700">
                <li className="flex items-start">
                  <CheckCircle className="w-5 h-5 mr-2 mt-0.5 flex-shrink-0 text-red-600" />
                  <span><strong>HTML/CSS/JavaScript</strong> - FreeCodeCamp (2 hrs/day). This is REQUIRED.</span>
                </li>
                <li className="flex items-start">
                  <CheckCircle className="w-5 h-5 mr-2 mt-0.5 flex-shrink-0 text-red-600" />
                  <span>Build simple webpage (your portfolio landing page)</span>
                </li>
                <li className="flex items-start">
                  <CheckCircle className="w-5 h-5 mr-2 mt-0.5 flex-shrink-0 text-red-600" />
                  <span>Research World Book products - explore worldbook.com</span>
                </li>
              </ul>
            </div>

            <div className="border-l-4 border-orange-500 pl-6 py-2">
              <h3 className="font-bold text-lg text-orange-700 mb-2">Week 2: Spring Boot + Project Start</h3>
              <ul className="space-y-2 text-slate-700">
                <li className="flex items-start">
                  <CheckCircle className="w-5 h-5 mr-2 mt-0.5 flex-shrink-0 text-orange-600" />
                  <span><strong>Spring Boot Tutorial</strong> - Build your first REST API</span>
                </li>
                <li className="flex items-start">
                  <CheckCircle className="w-5 h-5 mr-2 mt-0.5 flex-shrink-0 text-orange-600" />
                  <span>Start EdTech Project: "Study Quiz Web App" or "Digital Library"</span>
                </li>
                <li className="flex items-start">
                  <CheckCircle className="w-5 h-5 mr-2 mt-0.5 flex-shrink-0 text-orange-600" />
                  <span>Learn SQL basics for database integration</span>
                </li>
              </ul>
            </div>

            <div className="border-l-4 border-green-500 pl-6 py-2">
              <h3 className="font-bold text-lg text-green-700 mb-2">Week 3: Polish & Apply</h3>
              <ul className="space-y-2 text-slate-700">
                <li className="flex items-start">
                  <CheckCircle className="w-5 h-5 mr-2 mt-0.5 flex-shrink-0 text-green-600" />
                  <span>Complete your EdTech project with full documentation</span>
                </li>
                <li className="flex items-start">
                  <CheckCircle className="w-5 h-5 mr-2 mt-0.5 flex-shrink-0 text-green-600" />
                  <span>Update resume: Add "Technical Projects" & "Relevant Coursework"</span>
                </li>
                <li className="flex items-start">
                  <CheckCircle className="w-5 h-5 mr-2 mt-0.5 flex-shrink-0 text-green-600" />
                  <span>Polish GitHub: READMEs, descriptions, pin best 3 repos</span>
                </li>
                <li className="flex items-start">
                  <CheckCircle className="w-5 h-5 mr-2 mt-0.5 flex-shrink-0 text-green-600" />
                  <span>Write cover letter emphasizing EdTech passion + leadership</span>
                </li>
                <li className="flex items-start">
                  <CheckCircle className="w-5 h-5 mr-2 mt-0.5 flex-shrink-0 text-green-600" />
                  <span><strong>SUBMIT APPLICATION</strong></span>
                </li>
              </ul>
            </div>
          </div>
        </div>

        <div className="grid md:grid-cols-2 gap-6 mb-8">
          <div className="bg-gradient-to-br from-purple-100 to-purple-200 border-2 border-purple-400 rounded-lg p-6">
            <h3 className="font-bold text-xl text-purple-900 mb-3">Cover Letter Hook</h3>
            <div className="bg-white rounded p-4 text-sm text-slate-700 italic">
              "As someone who managed quality control for 7-person teams and created standardized processes, I understand that great products require both technical precision and clear documentation. I'm excited to bring this mindset—combined with my Java and Spring Boot skills—to World Book's EdTech mission of empowering students and teachers."
            </div>
            <p className="text-xs text-purple-800 mt-3">💡 Connects your leadership to their needs!</p>
          </div>

          <div className="bg-gradient-to-br from-blue-100 to-blue-200 border-2 border-blue-400 rounded-lg p-6">
            <h3 className="font-bold text-xl text-blue-900 mb-3">Interview Talking Points</h3>
            <ul className="space-y-2 text-sm text-slate-700">
              <li>✓ "I've been using Claude AI for coding assistance" (they want this!)</li>
              <li>✓ "My SOP experience taught me the value of documentation"</li>
              <li>✓ "Leading teams prepared me for code reviews & collaboration"</li>
              <li>✓ "I'm passionate about EdTech because..." (research World Book)</li>
            </ul>
          </div>
        </div>

        <div className="bg-yellow-50 border-2 border-yellow-300 rounded-lg p-6">
          <h3 className="font-bold text-xl text-yellow-900 mb-3">🎯 Your Competitive Advantage</h3>
          <p className="text-slate-700 mb-3">
            Most CS students applying will have <em>technical skills but no real-world leadership</em>. You have the reverse - and that's actually MORE valuable for an intern role where they expect to teach you tech but need mature, professional team players.
          </p>
          <div className="grid md:grid-cols-3 gap-3">
            <div className="bg-white rounded p-3 shadow-sm">
              <p className="font-semibold text-slate-800 text-sm">They Get:</p>
              <p className="text-xs text-slate-600 mt-1">Someone who shows up on time, communicates clearly, takes feedback well</p>
            </div>
            <div className="bg-white rounded p-3 shadow-sm">
              <p className="font-semibold text-slate-800 text-sm">You Stand Out:</p>
              <p className="text-xs text-slate-600 mt-1">3+ years professional experience vs. students with only classwork</p>
            </div>
            <div className="bg-white rounded p-3 shadow-sm">
              <p className="font-semibold text-slate-800 text-sm">Perfect Timing:</p>
              <p className="text-xs text-slate-600 mt-1">Feb 2026 graduation = summer 2026 internship = perfect!</p>
            </div>
          </div>
        </div>

        <div className="mt-6 text-center text-slate-600 text-sm">
          <p>💡 Click any card above to see more details • You're closer than you think!</p>
        </div>
      </div>
    </div>
  );
}
