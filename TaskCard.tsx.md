"use client";

import React from 'react';

interface TaskCardProps {
    title: string;
    description: string;
    dueDate: string;
    priority: 'High' | 'Medium' | 'Low';
}

const TaskCard: React.FC<TaskCardProps> = ({ title, description, dueDate, priority }) => {
    let priorityColor = 'bg-green-100 text-green-800';
    if (priority === 'High') {
        priorityColor = 'bg-red-100 text-red-800';
    } else if (priority === 'Medium') {
        priorityColor = 'bg-yellow-100 text-yellow-800';
    }

    return (
        <div className="bg-white rounded-md shadow-sm p-4">
            <h3 className="text-md font-semibold">{title}</h3>
            <p className="text-sm text-gray-500">{description}</p>
            <div className="flex items-center justify-between mt-2">
                <span className="text-xs text-gray-400">Due: {dueDate}</span>
                <span className={`px-2 py-1 rounded-full text-xs font-medium ${priorityColor}`}>{priority}</span>
            </div>
        </div>
    );
};

export default TaskCard;
