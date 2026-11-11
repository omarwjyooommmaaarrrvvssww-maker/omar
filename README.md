# omar
import { lstat, readdir, readFile } from "node:fs/promises"; import { extname, join, relative, resolve } from "node:path";  const reportDirectory = process.argv[2]; if (!reportDirectory) {     throw new Error("Usage: node validate-public-report.mjs &lt;report-directory>"); }  const allowedExtensions = new Set([".css", ".gif", ".html", ".ico", ".jpeg",
