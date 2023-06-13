<template>
    <form>
        <div class="mb-3">
            <label for="form-label">Issue</label>
            <input type="text" class="form-control" placeholder="Enter issue">
        </div>
        <div class="mb-3">
            <label for="form-label">Activity</label>
            <select>
                <option disabled value="">Select a type</option>
                <option value="">Web Aplication with Vue.js</option>
                <option value="">Backent sevice Node.js</option>
                <option value="">App Movile with React Native</option>
            </select>
        </div>
        <div class="mb-3">
            <label for="form-label">Issue</label>
            <input type="text" class="form-control" placeholder="Enter issue">
        </div>
        <div class="mb-3">
            <label class="form-check-label">Urgent </label>
            <input type="checkbox" form="form-check-input">
        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
    </form>
</template>