### **Git Tagging for Release Sustainability**  
Tagging commits helps in tracking releases, making it easy to revert, deploy, and manage software versions.

---

## **📌 Step 1: Create a Tag for an Old Commit**  
If you need to tag an **older commit**, first find its commit hash:  
```bash
git log --oneline
```
Example output:
```
f8ac4cd (HEAD -> hotfix-v1.0.0) EB-5433: (fix) Fixed a bug in the report generation
2b3a9f2 Previous release commit
```
Now, create a tag for the old commit:
```bash
git tag -a v1.0.0 -m "Tagging release v1.0.0" 2b3a9f2
```
- `-a v1.0.0` → Creates an **annotated** tag with the name `v1.0.0`.  
- `-m "Tagging release v1.0.0"` → Provides a message describing the tag.  
- `2b3a9f2` → The commit hash you want to tag.

---

## **🚀 Step 2: Create a Tag for the Latest Commit**  
If you want to tag the latest commit:
```bash
git tag -a v1.1.0 -m "Tagging latest release v1.1.0"
```
You don’t need a commit hash because it tags the current commit.

---

## **🌍 Step 3: Push Tags to the Remote Repository**  
To push a specific tag:
```bash
git push origin v1.0.0
git push origin v1.1.0
```
To push **all** tags at once:
```bash
git push origin --tags
```

---

## **🗑️ Step 4: Deleting a Tag (If Needed)**
If you need to delete a local tag:
```bash
git tag -d v1.0.0
```
If you need to delete it from the remote:
```bash
git push origin --delete v1.0.0
```

---

## **🔍 Step 5: Viewing Tags**
To list all tags:
```bash
git tag
```
To see tag details:
```bash
git show v1.0.0
```

---

## **🎯 Why Use Git Tags?**
✔ **Version Control:** Easily track releases (`v1.0.0`, `v1.1.0`).  
✔ **Reproducibility:** Revert to a specific release (`git checkout v1.0.0`).  
✔ **Deployment Management:** CI/CD pipelines can use tags for stable releases.  

Would you like a demo on checking out a tagged release? 😊