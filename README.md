## **Git Workflow and Pull Request (PR) Guidelines**

To ensure a smooth development process and avoid conflicts, it’s crucial to follow a standardized Git workflow and adhere to best practices for creating PRs. This document serves as a quick reference guide.

---

### **Git Workflow**

1. **Pull the Latest Develop Branch Daily**  
   - Start your day by pulling the latest changes from the `develop` branch.  
   - This ensures your local branch is up-to-date and minimizes merge conflicts.  

   ```bash
   git checkout develop
   git pull origin develop
   ```

---

### **2. Create Feature Branches for New Tasks**  
- Always create a new branch from `develop` for every feature or task.  
- Use a clear and consistent naming convention for branches, including the tracker ticket number.  
  - Example: `feature/123/task-name` or `bugfix/456/issue-name`.

```bash
git checkout -b feature/123/task-name
```

- This ensures better tracking and alignment with the corresponding tracker ticket.

--- 

3. **Commit Regularly and Push Frequently**  
   - Commit your changes frequently with clear, descriptive messages.  
   - Push your changes regularly to keep your progress visible and reduce the risk of data loss.

   ```bash
   git add .
   git commit -m "Descriptive commit message"
   git push origin feature/task-name
   ```

4. **Stay Updated to Minimize Merge Conflicts**  
   - Frequently merge the latest `develop` branch into your feature branch to stay aligned with team progress.

   ```bash
   git checkout develop
   git pull origin develop
   git checkout feature/task-name
   git merge develop
   ```

5. **Handle Merge Conflicts Promptly**  
   - If you encounter conflicts, resolve them promptly.  
   - Don’t hesitate to reach out for guidance if needed.

---

### **Pull Request (PR) Guidelines**

To streamline collaboration and maintain clarity, follow these steps when creating a PR:

1. **PR Description**  
   - Write a clear and detailed description of the changes made in your PR.  
   - Include context, purpose, and any specific notes for reviewers.

2. **Assign PR Labels**  
   - Add appropriate labels to your PR, such as `ready for review` or `in development`.

3. **Request a Review**  
   - Request a review from the ticket's accountable person promptly after creating the PR.  
   - Engage reviewers for faster feedback.

4. **Attach the Tracker Ticket Link**  
   - Link the tracker ticket associated with the task to your PR for better traceability.

5. **Update Ticket Status**  
   - Update the status of the tracker ticket to reflect the PR progress (e.g., "PR Raised").

6. **Attach PR Link to the Tracker Ticket**  
   - Copy the PR link and add it to the relevant ticket on the tracker system.

---

### **Additional Resources**  
For a detailed explanation of the Git workflow, refer to the [Git Workflow Guide](https://tracker.appfoster.com/projects/internal-operations/wiki/git-workflow).

---

By adhering to these guidelines, we can ensure consistent, efficient development and collaboration. Thank you for your efforts in maintaining these practices! 😊  

---
