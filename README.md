async function getUserPosts(userId) {
  try {
    console.log("Fetching user...");
    const user = await fetchUser(userId); // Takes 1 second
    console.log("Fetching posts...");
    const posts = await fetchPosts(user.id); // Takes 1 second
    console.log("Done");
    return posts;
  } catch (error) {
    console.error("Failed:", error);
  }
}

getUserPosts(123);
console.log("Function called");
