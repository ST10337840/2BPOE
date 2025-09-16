using CMCS.Models;
using Microsoft.EntityFrameworkCore;
using System;
using System.Collections.Generic;


internal class Program
{
    private static void Main(string[] args)
    {
        {
}
        ProjectPlanDemo.Run(); ProjectPlanDemo.Run();
    }

public class ProjectPlanDemo
    {
        public static void Run()
        {
            var tasks = new List<ProjectTask>
            {
                new ProjectTask { TaskId = 1, Name = "Requirements Review", Details = "Analyse POE brief, rubric, and features", Dependencies = "None", DurationDays = 1, StartDay = 1 },
                new ProjectTask { TaskId = 2, Name = "Database Design (UML)", Details = "Define entities and relationships", Dependencies = "Task 1", DurationDays = 2, StartDay = 2 },
                new ProjectTask { TaskId = 3, Name = "Documentation (Design Choices)", Details = "Write rationale for DB and GUI layout", Dependencies = "Task 2", DurationDays = 1, StartDay = 3 },
                new ProjectTask { TaskId = 4, Name = "GUI Prototype", Details = "Create WPF/MVC front-end screens", Dependencies = "Task 2, Task 3", DurationDays = 3, StartDay = 4 },
                new ProjectTask { TaskId = 5, Name = "Project Plan", Details = "Prepare Gantt and task breakdown", Dependencies = "Task 1–4", DurationDays = 1, StartDay = 5 },
                new ProjectTask { TaskId = 6, Name = "GitHub Version Control", Details = "Create repo, commit 5+ times", Dependencies = "Ongoing", DurationDays = 9, StartDay = 2 },
                new ProjectTask { TaskId = 7, Name = "Report Draft", Details = "Compile report (400–500 words)", Dependencies = "Task 1–5", DurationDays = 2, StartDay = 7 },
                new ProjectTask { TaskId = 8, Name = "Final Review & Submission", Details = "Proofread and submit", Dependencies = "Task 7", DurationDays = 2, StartDay = 9 }
            };

            Console.WriteLine("📋 Contract Monthly Claim System – Project Plan\n");
            foreach (var task in tasks)
            {
                Console.WriteLine(task);
            }
        }
    }
}


